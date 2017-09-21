# **第一篇：web前端教程**

## 第一节 知识准备

---

### 1.1 何为web前端

`web`前端（以下无特殊说明，都简称为**前端**）归属“`IT`行业 - 软件开发 - 浏览器端系统开发（`B/s`模式） - `web`前端开发”。

### 1.2 初学要求

- 学历：建议大专或以上

- 年龄：28周岁以下

- 时间
	- 自学：找到好的教程 + 好的学习路线 + 每天3小时有效学习 + 总耗时半年以上
	- 培训：找到合适的培训机构 + 好的老师带 + 每天8小时有效学习 + 总耗时4个月

- 性格：能静下来看文档或视频

### 1.3 了解一些知识点

1. 网址：如`http://www.baidu.com`，又成为“url地址”
2. 文件格式：又称“后缀名”，如图片格式为`.png`、`.jpg`、`.gif`等，文档格式有`.txt`、`.docx`、`.ppt`等。前端行业也有一些特定的文件格式，比如`.html`、`.css`和`.js`。
3. 编辑器：写不同的文件会使用不同的编辑器，如写`word`文档用`office word`。前端开发代码也有专门的编辑器（复杂且强大的编辑器又称`IDE`），如`sublime`和`webstorm`等。

## 第二节 第一个代码

---

### 2.1 Hello World 页面

> 新建文件

鼠标点击右键新建一个文本文档，重命名为`hello world.html`。使用`sublime`编辑器打开文档，再将以下代码复制粘贴进去，按住`Ctrl + S`保存。

```HTML
<!DOCTYPE html>
<html>
<head>
	<meta charset="UTF-8">
	<title>标题</title>
</head>
<body>
	Hello World !
</body>
</html>
```

> 查看效果

在浏览器里面打开上述文件，看一下显示出来的是什么

!> 对于文件的命名有几个要求：a.开头必须是英文或下划线_或$符号  b.建议使用驼峰命名法（helloWorld.html）或中横线法（hello-world.html）

!> 一般不做特殊说明，教程里面使用的浏览器都是最新的`chrome`

### 2.2 网页的几个重要认识


> 文件后缀名

网页文件默认的后缀名是`.html`，但有些地方也会见到`.htm`或者`.shtml`，作为初学者暂时不要理会，先约束自己严格按照`.html`后缀执行即可。

> 网页文件

**只有`.html`文件才是网页文件**，未来会接触到的`.css`、`.js`甚至后端的`.py`、`.php`等都不是网页文件。浏览器只能识别`.html`文件，其他的文件要不是嵌入到`.html`文件中，要不是经过编译后转成`.html`文件才能被浏览器识别。


## 第三节 HTML知识点

---

### 3.1 标签与属性

html文件是由“标签”、“标签属性”与“内容”三部分组成的。

```HTML
<div id="app"> 这里写内容 </p>
```

> 标签

标签是“尖括号括起来的字符串”，如`<div>...</div>、<p>...</p>、<img>`。

- 双标签：有些标签有启示部分和结束部分，内容写在两者之间，如`<p>内容</p>`。
- 单标签：有些标签却只有开始部分，内容一般都是由标签内部的属性引入，如`<img src="./cat.jpg">`。

> 属性

写在**起始标签**里面，一般给赋上一定的值，用来强化标签，如`<img src="./cat.jpg" alt="这是图片">`，其中alt属性表示“当图片不能正常显示时候，用文字**这是图片**来替代图片提示用户这里是图片”。

### 3.2 常用标签分类记忆法

!> `html`常用的标签有几十个，对于初学者来说要一次性记住这么多确实有一定困难，但是又必须要记住！在这里可以尝试这种记忆方法，如下。

| 标签分类      | 标签特征               | 常用标签  |
| :------------- |:-----------------------| :---------------|
| 结构标签      | html页面结构的构建     | html、body、head、meta、title、script、style、link |
| 块状标签      | 独立占据整行           | div、p、ul、ol、li、hr、h1-h6 |
| 行内标签      | 不占据一整行           | span、img |
| 表单标签      | 表单家族，用作数据提交 | form、input、select、option、textarea、button |
| 表格标签      | 表格家族，用作数据展示 | table、thead、tbody、caption、tr、th、td |
| 文字修饰标签  | 修饰文字               | b、strong、em、i、u、s、sup、sub |

> 上述表格的附加说明

1. 上表的分类方法，能够较好的记忆标签。但这样分类有些标签有可能符合多个类别，如“文字修饰标签”其实都属于“行内标签”，表单和表格的部分标签也同时属于“块状标签”范畴，这里我们在初学阶段先按上表的方法来记忆，等使用熟练了自然就懂了。
2. 有些标签是需要**成组使用**的，如`select-option`、`ul-li`、`ol-li`，单独出现意义不大。

> 几个重要标签讲解（需要重视）

- `h1`标签：表示最大的标题标签，在一个页面里面`h1`标签只能出现一次。
- `img`标签：`img`标签归类为“行内标签”，但是和普通的行内标签不同，`img`标签还具有自己的`width`和`height`属性。
- `button`标签：按钮标签，button标签如果不写type属性为button的话，在一些浏览器里面会默认触发form的action。
- `hr`标签：一根直线，可以对其设置宽高度，但是会有默认的内陷边框（设置border: none;解决）

### 3.3 html代码注释

!> html代码注释的意思是：“使注释的部分不运行且不影响其他代码的运行”，注释符为 <!-- 这里是需要注释的内容 -->

> 在html中，有以下情况需要注释代码

- 有些代码不需要其运行，但是又不想删除；
- 给代码添加一些注释或说明文字，却不能影响代码；
- 注释实例

```HTML
<!DOCTYPE html>
<html>
<head>
	<meta charset="UTF-8">
	<title>标题</title>
</head>
<body>
	<div id="app"><!-- 离离原上草， -->一岁一枯荣。</div>
	<!-- <p>野火烧不尽，春风吹又生。</p> -->
</body>
</html>
```

以上代码显示的内容是：一岁一枯荣。

## 第四节 CSS知识点

---

### 4.1 css格式与引入方式

> **css格式**，如下所示

```HTML
div { width: 100px; height: 200px; color: #cccccc; }
```

![img](static/imgs/selector.gif)

其中

- h1为selector，选择器
- color为property，属性
- blue为value，值
- color: blue; 何在一起为declaration，样式申明；多个样式之间用分号隔开

> **css的引入方式**，即css写在哪里？css有三种写法

- 标签行内：直接将css写在标签内部，使用style标签包裹起来

```HTML
...
<div style="color: red;">这是css样式写在标签内的例子</div>
...
```

- 内部引用：写在head标签中间，使用style标签包裹起来

```HTML
...
<head>

<style>
div { color: red; }
</style>

</head>
<body>
...
</body>
```

- 外部引入：将css单独保存为.css文件，然后通过link标签引入到html文件中

```HTML
...
<head>

<link rel="stylesheet" href="main.css">

</head>
<body>
...
</body>
```

这是外部的main.css文件

```CSS
div { color: red; }
```

### 4.2 文件路径问题

> 相对路径

相对路径，即不完整路径（不带协议头），不会随着项目文件夹的迁移而失效。
相对路径有以下几种，根据实际场景选择使用。

- `./abc.html`：当前目录下的`abc.html`文件
- `/abc.html`：根目录下的`abc.html`文件
- `../abc.html`：与上级目录同级的`abc.html`文件
- `abc.html`：当前目录下的`abc.html`文件

> 绝对路径

绝对路径，表示完整的路径，一般带有协议头（`url`路径协议头为`http`或`https`，磁盘路径协议头为`file`），如下

- `http://www.baidu.com/abc.html` 
- `d://index/abc.html`   ---> 表示：d盘index文件夹下的abc.html文件

!> 在实际开发中，除了`cdn`文件（`js`、`css`或部分网络图片）使用绝对路径（`url`路径）外，其他的文件都默认使用相对路径。

## 第五节 HTML和CSS版本的问题

### 5.1 HTML版本

本篇主要讲解的是`html4.01`版，最新的版本是`html5`。`html5`在`html4.01`版本的基础上，做了一些标签增加和属性强化。关于`html5`版本在第三篇中重点讲解，本篇只做简单了解。

- 新增了一些语义化标签：`header`、`footer`、`nav`、`aside`、`article`、`section`等
- 强化了一些属性：如`input`标签的`type`属性值扩充了`number`、`time`等
- 增加了一些功能标签：`canvas`、`svg`等 

### 5.2 CSS版本

本篇涉及的是css2.0版，最新的是css3。新版相对与老版本增加了许多的功能，在第三篇中再细讲。

!> 很多同学会有一个疑问，为什么不直接学习`html5`和`css3`？<br><br>两个原因：<br>  一是，`html5`和`css3`在一些旧版本浏览器中不兼容；<br>  二是，新版本只是在老版本的基础上做了一些增加和强化，绝大部分的知识点还是以老版本为主。<br><br>所以，学习老版本是很有必要的，实际应用范围更广，新版本在后续篇章中再做补充。

----

## 第六节 语义化编程习惯

----

### 6.1 取名

> 取名规则

取名，主要是`css`的`class`和`id`类名、`js`的变量和函数名等，要根据其效果或作用来取名字。取出来的名字，让读者大致的领会到其意义。

- 首字母：大小写英文字母 或 _  或 $，只能是这几种。（强烈建议，小写字母开头！）
	- 大写字母开头：一般都是类名、构造函数名
	- 下划线_开头：一般都是魔术方法、系统常量或探针
	- $符号开头：一般是变量
- 全名
	- 语义化：如“文章列表”叫`article-list`、`article_list`、`articleList`、`ArticleList`
	- 多单词规则：小驼峰、大驼峰、中横线和下横线四种


### 6.2 注释

> 局部注释：某个变量、某段代码，写个注释说明一下用法

```HTML
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>wcodeplus</title>
  <meta name="description" content="Description">
  <link rel="stylesheet" href="./static/vue.css">
</head>
<body>
  <!-- 注释1：这个nav标签，表示文档顶部的中英文切换 -->
  <nav>
      <a href="#/">EN</a>
      <a href="#/zh-cn/">中文</a>
  </nav>
  <div id="app"></div>
</body>
<script>
  window.$docsify = {
    name: '',
    repo: ''
  }
</script>
<!-- 注释2：下面引入的是docsify的js文件，如果要修改需要下载未压缩版本 -->
<script src="./static/docsify.min.js"></script>
</html>
```

> 整体注释：一个类或函数，里面有很多变量、参数和方法，需要一起说明（有时还会加上作者信息等）

```php
<?php
// +----------------------------------------------------------------------
// | OneThink [ WE CAN DO IT JUST THINK IT ]
// +----------------------------------------------------------------------
// | Copyright (c) 2013 http://www.onethink.cn All rights reserved.
// +----------------------------------------------------------------------
// | Author: 麦当苗儿 <zuojiazi@vip.qq.com> <http://www.zjzit.cn>
// +----------------------------------------------------------------------

namespace Home\Controller;

/**
 * 文档模型控制器
 * 文档模型列表和详情
 */
class ArticleController extends HomeController {

    /* 文档模型频道页 */
	public function index(){
		/* 分类信息 */
		$category = $this->category();

		//频道页只显示模板，默认不读取任何内容
		//内容可以通过模板标签自行定制

		/* 模板赋值并渲染模板 */
		$this->assign('category', $category);
		$this->display($category['template_index']);
	}

	/* 文档模型列表页 */
	public function lists($p = 1){
		/* 分类信息 */
		$category = $this->category();

		/* 获取当前分类列表 */
		$Document = D('Document');
		$list = $Document->page($p, $category['list_row'])->lists($category['id']);
		if(false === $list){
			$this->error('获取列表数据失败！');
		}

		/* 模板赋值并渲染模板 */
		$this->assign('category', $category);
		$this->assign('list', $list);
		$this->display($category['template_lists']);
	}

	/* 文档模型详情页 */
	public function detail($id = 0, $p = 1){
		/* 标识正确性检测 */
		if(!($id && is_numeric($id))){
			$this->error('文档ID错误！');
		}

		/* 页码检测 */
		$p = intval($p);
		$p = empty($p) ? 1 : $p;

		/* 获取详细信息 */
		$Document = D('Document');
		$info = $Document->detail($id);
		if(!$info){
			$this->error($Document->getError());
		}

		/* 分类信息 */
		$category = $this->category($info['category_id']);

		/* 获取模板 */
		if(!empty($info['template'])){//已定制模板
			$tmpl = $info['template'];
		} elseif (!empty($category['template_detail'])){ //分类已定制模板
			$tmpl = $category['template_detail'];
		} else { //使用默认模板
			$tmpl = 'Article/'. get_document_model($info['model_id'],'name') .'/detail';
		}

		/* 更新浏览数 */
		$map = array('id' => $id);
		$Document->where($map)->setInc('view');

		/* 模板赋值并渲染模板 */
		$this->assign('category', $category);
		$this->assign('info', $info);
		$this->assign('page', $p); //页码
		$this->display($tmpl);
	}

	/* 文档分类检测 */
	private function category($id = 0){
		/* 标识正确性检测 */
		$id = $id ? $id : I('get.category', 0);
		if(empty($id)){
			$this->error('没有指定文档分类！');
		}

		/* 获取分类信息 */
		$category = D('Category')->info($id);
		if($category && 1 == $category['status']){
			switch ($category['display']) {
				case 0:
					$this->error('该分类禁止显示！');
					break;
				//TODO: 更多分类显示状态判断
				default:
					return $category;
			}
		} else {
			$this->error('分类不存在或被禁用！');
		}
	}

}

```