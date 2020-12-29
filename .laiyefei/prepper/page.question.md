---
layout: default
---

<link rel="stylesheet" type="text/css" href="/assets/css/biz/question.buff.css" />

<div>	
	<section class="container">
	<div class="content-wrap">
		<div class="content csSecContent" >
		  <div class="title csTitleContent" style=" border-bottom: 1px solid black;padding:10px;box-shadow: 0 1px 2px grey">
			<h3 style="line-height: 1.3;font-weight: bold;">ℒ　问题仓库</h3>
		  </div>
		<section id="cd-timeline" class="cd-container dv_question">
			{% for post in site.posts  %}
			<div class="container">
				<div class="card" style="--cards:5;">
					<div class="child">
					<h2>{{ post.title }}</h2>
					<h3>{{ post.note }}</h3>
					<p>{{ post.date | date: '%Y-%m-%d' }}
						<span>{{ post.categories }}</span>
					</p>
					</div>
					<div class="child"></div>
					<div class="child"></div>
					<div class="child"></div>
					<div class="child"></div>
				</div>
			</div> 
			{% endfor %}
		</section>  
		</div>
	</div>
	 <aside class="sidebar">
		<div class="fixed">
			<div class="widget widget_hot">
				<div>{% include tag.wall.md titleColor="pink" title="✠ 问题归类 " %}</div>
			</div>
		</div>
	</aside>

</section>

</div>
