---
layout: default
---
<div>
	<section class="container">
	<div class="content-wrap">
	<div class="content">
	  <div class="title" style=" border-bottom: 1px solid black;padding:10px;box-shadow: 0 1px 2px grey">
		<h3 style="line-height: 1.3">ஐ 图书馆</h3>
	  </div>
	  <div>
	  	<iframe id="iframeBody" name="iframeBody" src="/views/mix/pdfjs/web/viewer.html?file={{ '/books/quantum1.pdf' | prepend: site.warehouse }}" style="width:100%;height: 100%;border:none;box-shadow: 0 0 10px grey">
	  	</iframe>
	  </div>   
	  <nav class="pagination" style="display: none;">
		<ul>
		  <li class="prev-page"></li>
		  <li class="active"><span>1</span></li>
		  <li><a href="?page=2">2</a></li>
		  <li class="next-page"><a href="?page=2">下一页</a></li>
		  <li><span>共 2 页</span></li>
		</ul>
	  </nav>
	</div>
	</div>
	<aside class="sidebar">
		<div class="fixed">
			<div class="widget widget_hot">
				{% include tree.book.html %}
			</div>
		</div> 
	 </div>   
	</aside>
</section>


<script type="text/javascript">
	;(function(){
	$("html, body").css({
		"overflow":"hidden"
	});
	//iframeBody
	$("#iframeBody").height(window.screen.height - 290);
})();
</script>
<script type="text/javascript">
	(function(){
		var screenHeight = window.screen.height;
		var $dvToc = $(".csToc");
		var maxHeight = (screenHeight - 250);
		$dvToc.css({
			"max-height" : maxHeight + "px"
		});  
		$("blockquote p").css({
			"text-indent" : 0
		});
		var nowHeight = $dvToc.height();
		$dvToc.height(nowHeight + 20)
	})();
</script>
</div>