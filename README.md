WordPressPet
=======

浮动小人 WordPress博客宠物

作者
------------

木木

使用说明
-------

+ 下载 `spig.js` 和 `spig.png` ，放在网站任意目录下

+ 把下面代码加到`footer.php`文件的body里,注意修改 `spig.js路径` 和 `spig.png路径`

```
	<!--.浮动小人-->
	<script type="text/javascript">
		<?php if(is_home()) echo 'var isindex=true;var title="";';else echo 'var isindex=false;var title="',  get_the_title(),'";'; ?>
		<?php if((($display_name = wp_get_current_user()->display_name) != null)) echo 'var visitor="',$display_name,'";'; else if(isset($_COOKIE['comment_author_'.COOKIEHASH])) echo 'var visitor="',$_COOKIE['comment_author_'.COOKIEHASH],'";';else echo 'var visitor="游客";';echo "\n"; ?>
	</script>
	<script type="text/javascript" src="spig.js路径"></script>
	<style>
		.spig {display:block;width:130px;height:170px;position:absolute;bottom: 300px;left:160px;z-index:9999;}
		#message{color :#191919;border: 1px solid #c4c4c4;background:#ddd;-moz-border-radius:5px;-webkit-border-radius:5px;border-radius:5px;min-height:1em;padding:5px;top:-45px;position:absolute;text-align:center;width:auto !important;z-index:10000;-moz-box-shadow:0 0 15px #eeeeee;-webkit-box-shadow:0 0 15px #eeeeee;border-color:#eeeeee;box-shadow:0 0 15px #eeeeee;outline:none;}
		.mumu{width:130px;height:170px;cursor: move;background:url(spig.png路径) no-repeat;}
	</style>
	<div id="spig" class="spig">
		<div id="message">加载中……</div>
		<div id="mumu" class="mumu"></div>
	</div>
	<!--.end浮动小人-->
```

+ 使用前需要加载jQuery库

+ 个性化

1.基本信息(必选)

	`spig.js` 第10行 第57行 改成你自己网站的信息

2.修改大小

	上述代码第10行 `width` `height` 参数


3.停留位置

	`spig.js` 第147行 第240行 `s` 参数

Blog
-------
+ [给网站加一个浮动小人—wordpress博客宠物（不知道是不是叫这个名字…）](http://www.anotherhome.net/785)
