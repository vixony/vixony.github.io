使用gulp自动化前端工作流

安装gulp
gulp推荐安装到项目目录，不推荐全局目录，因为后期gulp会自动引入项目相关的支持包，如果全局安装gulp，这些支持包全都安装在/usr/local/lib/node_modules/下，不利于管理，可能易引起冲突。

npm install gulp
安装常用插件
// js压缩
gulp-uglify
// css压缩
gulp-clean-css
// 重命名
gulp-rename
// 合并文件
gulp-concat
// 捕获错误
gulp-plumber
// 打包
gulp-zip
//过率console信息
gulp-strip-debug
在gulpfile.js中载入插件
var gulp = require('gulp');
var uglify = require('gulp-uglify');
var concat = require('gulp-concat');
var minifyCss = require('gulp-minify-css');
var rename = require('gulp-rename');
var plumber  = require('gulp-plumber');
var zip = require('gulp-zip');
var browserSync = require('browser-sync');
自动压缩css重命名
定义一个任务compress-css,压缩static文件夹下面的index.css,并且重命名为index.min.css,保存到build文件夹下面

gulp.task('compress-css', function() {
    gulp.src('static/index.css')
        .pipe(minifyCss())
        .pipe(rename('index.min.css')) 
        .pipe(gulp.dest('build'));
});
自动压缩js代码并且重命名
定义一个任务compress-js,压缩static文件夹下面的index.js,并且重命名为index.min.js,保存到build文件夹下面

gulp.task('compress-js', function() {
    gulp.src('static/index.js')
        .pipe(uglify())
        .pipe(rename('index.min.js')) 
        .pipe(gulp.dest('build'));
});
自动合并文件
合并src下面的js文件，重命名为all.js，保存在build文件夹下面

gulp.task('minify', function (){
     return gulp.src('src/*.js')
        .pipe(concat('all.js'))
        .pipe(gulp.dest('build'))
});
执行某个任务
gulp teskname
监视文件变化
这里定义一个默认的任务，只需要在gulp里面输入gulp

gulp.task('default', function(){
    gulp.watch('src/*.*', function(){
        gulp.run('teakname')
    });
});

打包发布任务
新建任务zip，将build文件夹下面的文件全部打包为publish.zip,发布到release文件夹下面

gulp.task('zip', function(){
    return gulp.src('build/*')
        .pipe(plumber())
        .pipe(zip('publish.zip'))
        .pipe(gulp.dest('release'))
});
自动刷新浏览器
新建任务start，启用一个本地server，监视当前目录下的所有文件，一旦文件变化，浏览器reload

gulp.task('start', function() {
    browserSync.init({
        server: {
            baseDir: "./"
        }
    });

    gulp.watch('./*', function() {
        browserSync.reload();
    });
})
在build任务中过滤目标文件中的console.log();
var stripDebug = require('gulp-strip-debug');
gulp.task('build', function () {
        .gulp.src()
        .pipe(stripDebug())
        .pipe(gulp.dest());
});
监听gulp任务结束,执行回调
gulp.task('dev', function(){
    gulp.src(src)
        .pipe(rename('app.js'))
        .on('end',function(){
           console.log('这里是回调')
        })

});
2015年12月23日发布

- 1、run-sequence
Links: https://www.npmjs.com/package/run-sequence
作用：让gulp任务，可以相互独立，解除任务间的依赖，增强task复用

2、browser-sync
Links: http://www.browsersync.io/
作用：静态文件服务器，同时也支持浏览器自动刷新

3、del
Links：https://www.npmjs.com/package/del
作用：删除文件/文件夹

4、gulp-coffee
Links: https://github.com/wearefractal/gulp-coffee
作用：编译coffee代码为Js代码，使用coffeescript必备

5、coffee-script
Links: https://www.npmjs.com/package/coffee-script
作用：gulpfile默认采用js后缀，如果要使用gulpfile.coffee来编写，那么需要此模块

6、gulp-nodemon
Links: https://www.npmjs.com/package/gulp-nodemon
作用：自动启动/重启你的node程序，开发node服务端程序必备

7、yargs
Links: https://www.npmjs.com/package/yargs
作用：用于获取启动参数，针对不同参数，切换任务执行过程时需要

8、gulp-util
Links: https://www.npmjs.com/package/gulp-util
作用：gulp常用的工具库

9、gulp-uglify
Links: https://www.npmjs.com/package/gulp-uglify
作用：通过UglifyJS来压缩JS文件

9、gulp-concat
Links: https://www.npmjs.com/package/gulp-concat
作用：合并JS

10、gulp-sourcemaps
Links: https://www.npmjs.com/package/gulp-sourcemaps
作用：处理JS时，生成SourceMap

11、gulp-less
Links：https://www.npmjs.com/package/gulp-less
作用：将less预处理为css

12、gulp-sass
Links：https://www.npmjs.com/package/gulp-sass
作用：将sass预处理为css

13、gulp-autoprefixer
Links：https://www.npmjs.com/package/gulp-autoprefixer
作用：使用Autoprefixer来补全浏览器兼容的css。

14、gulp-minify-css
Links：https://www.npmjs.com/package/gulp-minify-css
作用：压缩css。

15、connect-history-api-fallback
Links：https://www.npmjs.com/package/connect-history-api-fallback
作用：开发angular应用必须，用于支持HTML5 history API.
