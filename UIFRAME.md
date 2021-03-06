## 基础web控件
- 图标 ： icon库（iconfont，base64，svg等）元素库
- 按钮 ： 基本的按钮
- 进度条 ： 进度比例的可视化动态展示
- 标签 ： 线性标签的样式化显示
- 表单控件 ： 统一的表单组合
- 输入框 ：
- 选择框 ：
- 按钮 ：
- 多选和单选框 ：
- 开关 ：
- 提示引导：面包屑 - title提示 - 模拟提示
- 图片 ： 图片的基本显示控制，适配容器缩放，默认显示，懒加载控制
- 多级标题 ： h1，h2, h3, h4, h5, h6
- 分隔线 ： 多样式的内容分割线控制
- 滚动条 ： 滚动条的美化

## 修饰组件
- 输入框 ： 基本的输入表单标签
- 标签，图标，搜索，常态，激活（鼠标经过），禁用
- 消息框 ： 文档流当中的消息样式显示展示一些需要引起用户注意的内容。
- 代码 ： 针对代码的格式化显示
- 输入组 ： 标题，按钮，选项及输入的组合显示 
- 列表组 ： 用于显示基本有序无序列表元素的基本样式，ul，ol等
- 菜单导航 ： 导航标签组合，	
- 导航条 ： 导航条的显示
- 垂直菜单 ： 基本的展开菜单
- 分页条 ： 分页显示序列
- 面板 ： 基本的内容面板，标题，内容，注脚等
- 表格 ： 基本的 表格样式，无线表格，细线表格，横线表格，分行背景色表格，等
- 按钮组 ： 多按钮的组合，按钮组，分组，垂直排列，下拉显示，弹层显示等按钮


## 交互JS插件
- 搜索框 ： 输入，选择，搜索，筛选预加载
- 分页 ： 分页显示器，用于导航标签多页面内容
- 本地存储 : 页面存储，cookies，indexDB，localstorage，sessionstorage
- 复制内容 : 复制标签的内容，或者选定的文本，图片以及标签等。
- 选择器 : select模拟下拉选框，统一的视觉和交互
- 日期选择 ： 简约的日期选择，结合日历控件
- 颜色选择器 - 用于主题，色彩标记等的选项设定
- 下拉菜单 ： select下来菜单（一定数量的选项）
- 排版选择 ： 选择不同的主题，版式等的显示状态
- 标签页 ： 通过点击一个导航或列表项目来切换显示的内容，
- 弹出层 ： 用于独立于页面文档流的内容浮动显示具体如下：
	- 对话框触发器 ： 按钮标签等选项的可配置触发器
	- 上下文菜单 ： 用于显示当前操作上下文可扩展的交互选项
	- 漂浮消息 ： notify浮动独立显示弹层
	- 模态对话框 ： 标题，关闭，操作按钮，取消按钮，正文显示，消息提示，
	- 提示消息 ： tips跟随内容旁注显示弹出浮动标签 较少内容的提示，浮动，不浮动，显示在触发元素周边，上下左右
	- 弹出面板 ： popover独立弹出层，用户较多内容的独立弹层，浮动，不浮动，显示在触发元素周边，上下左右
- 折叠展开 - 内容的扩展显示和折叠隐藏 
- 轮播滚动slide ： 画面容器的切换浏览和自动轮播，
- 图片浏览 ： 
- 富文本编辑器 ： 编辑图文内容，插入多媒体内容，图片上传，贴图上传等
- 拖动 ： 拖动元素在页面范围内移动 
	- 拖拽控制 ： 拖拽拖放操作的基本事件监控
	- 拖放排序 ： 拖拽内容框到目标区域，实现元素的位移，排序等
	- 拖拽选取 ： 拖拽选定覆盖的元素或者内容
- 滚动识别 ： nicescroll滚动选择 模拟滚动，实体滚动，

## 页面视图模块
- 数据表格 ： 数据显示、排序、搜索以及海量数据显示。
- 标签页管理器 ： 主要用于页签管理,区别于tab切换
- 树形菜单 ： 用于侧边栏的树形结构层级菜单
- 文件上传 ： 展示层级关系（例如文件系统目录）菜单的视图。
- 日历 ： 提供日期选择，日志标记等，
- 表单 ： 用户交互界面中，提供输入交互入口
- 文章 ： 用于图文混编多媒体展示等的文章展示结构。包含 标题 ,简介，其他额外信息,图文内容,音视频等多媒体内容。
- 卡片 ： 卡片视图使用网格（栅格）来集中展示一组卡片结构。
- 列表 ： 列表视图用于展示一组包含图文的内容。
- 评论 ： 评论视图用于展示评论消息，评论列表允许进行嵌套。包含 评论的用户头像，评论内容的容器，相关操作（回复、删除，编辑，点赞等）
- 图表chart ： 用户数据的可视化展示
- 组合看板 ： 管理多个容器及子条目，允许用户通过拖拽为字条目排序，并将条目从一个容器拖动到另一个容器。
	拖动时会在文档中插入被拖动元素的影子元素，会跟随鼠标光标位置，用于指示当前拖动的位置。
- 仪表盘 ： 多个面板组（.panel）并配合栅格来展现内容的方式。
- 滚动浏览 ： 图片的预览，轮动等
	- 结合swiper，实现卡片式轮动
	- fullpage滚动

 
