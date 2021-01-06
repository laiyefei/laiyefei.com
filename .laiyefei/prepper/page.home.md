---
layout: default
title: 首页
permalink: /index
---


<div>
    <section class="container">
        <div class="content-wrap">
            <div class="content">
                <div id="focusslide" class="carousel slide" data-ride="carousel">
                    <ol class="carousel-indicators">
                        <li data-target="#focusslide" data-slide-to="0" class="active"></li>
                        <li data-target="#focusslide" data-slide-to="1"></li>
                        <li data-target="#focusslide" data-slide-to="2"></li>
                        <li data-target="#focusslide" data-slide-to="3"></li>
                        <li data-target="#focusslide" data-slide-to="4"></li>
                    </ol>
                    <div class="carousel-inner" role="listbox" title="心之所向">
                        <div class="item active">
                            <a href="javascript:;"  title="量子纠缠">
                                <img src="/assets/img/system/home/lzjc.jpg" alt="量子纠缠" class="img-responsive"></a>
                        </div>
                        <div class="item">
                            <a href="javascript:;"  title="天空之城">
                                <img src="/assets/img/system/home/sky.jpg" alt="天空之城" class="img-responsive"></a>
                        </div>
                        <div class="item">
                            <a href="javascript:;"  title="听风">
                                <img src="/assets/img/system/home/listening.jpg" alt="听风" class="img-responsive"></a>
                        </div>
                        <div class="item">
                            <a href="javascript:;"  title="海角天涯">
                                <img src="/assets/img/system/home/love.jpg" alt="海角天涯" class="img-responsive"></a>
                        </div>
                        <div class="item">
                            <a href="javascript:;"  title="诗与远方">
                                <img src="/assets/img/system/home/see.jpg" alt="诗与远方" class="img-responsive"></a>
                        </div>
                    </div>
                    <a class="left carousel-control" href="#focusslide" role="button" data-slide="prev" rel="nofollow">
                        <span class="glyphicon glyphicon-chevron-left" aria-hidden="true"></span> <span
                            class="sr-only">上一个</span> </a> <a class="right carousel-control" href="#focusslide"
                        role="button" data-slide="next" rel="nofollow"> <span class="glyphicon glyphicon-chevron-right"
                            aria-hidden="true"></span> <span class="sr-only">下一个</span> </a>
                </div>
                <article class="excerpt-minic excerpt-minic-index">
                    <h2><span class="red">【推荐】</span><a target="_self"
                            href="{{ site.posts.first.url | prepend: site.baseurl | prepend: site.url }}"
                            title="{{site.posts.first.title}}">{{site.posts.first.title}}</a>
                    </h2>
                    <p class="note">
                        {{site.posts.first.note}}
                    </p>
                </article>
                <div class="title">
                    <h3 style="color:grey">最新发布</h3>
                    <div class="more">
                        <a href="javascript:;" title=""></a>
                    </div>
                </div>
                {% for post in paginator.posts %}
                <article class="excerpt excerpt-1" style="">
                    <a class="focus" href="javascript:;" title="{{post.title}}" target="_self"><img class="thumb"
                            data-original="/assets/img/posts/{{ post.date | date: "%Y-%m-%d" }}/title.jpg"
                            src="/assets/img/biz/title/{{ post.date | date: "%Y-%m-%d" }}.jpg" alt="{{post.title}}"
                            style="display: inline;"></a>
                    <header><a class="cat" href="javascript:;" title="{{ post.categories }}">{{ post.categories
                            }}<i></i></a>
                        <h2>
                            <a href="{{ post.url | prepend: site.baseurl | prepend: site.url }}" title="{{post.title}}"
                                target="_self">{{post.title}}</a>
                        </h2>
                    </header>
                    <p class="meta">
                        <time class="time"><i class="glyphicon glyphicon-time"></i>
                            {{ post.date | date: "%Y-%m-%d" }}
                        </time>
                    </p>
                    <p class="note">
                        {{post.note}}
                    </p>
                </article>
                {% endfor %}
                <nav class="pagination" style="display: none;">
                    <ul>
                        {% if paginator.total_pages > 1 %}
                        {% if paginator.previous_page %}
                        <li class="prev-page"><a
                                href="{{ paginator.previous_page_path | prepend: site.baseurl | prepend: site.url }}"
                                aria-label="Previous"><span aria-hidden="true">&laquo;</span></a></li>
                        {% endif %}
                        {% for page in (1..paginator.total_pages) %}
                        {% if page == paginator.page %}
                        <li class="active"><span>{{ page }}</span></li>
                        {% elsif page == 1 %}
                        <li><a href="{{ '/' | prepend: site.baseurl | prepend: site.url  }}">{{ page }}</a></li>
                        {% else %}
                        <li><a href="{{ page |  prepend: '/' | prepend: site.baseurl | prepend: site.url }}">{{ page
                                }}</a></li>
                        {% endif %}
                        {% endfor %}
                        {% if paginator.next_page %}
                        <li class="next-page"><a
                                href="{{ paginator.next_page_path | prepend: site.baseurl | prepend: site.url }}"
                                aria-label="Next"><span aria-hidden="true">&raquo;</span></a></li>
                        {% endif %}
                        {% endif %}
                        <li><span>共 {{ paginator.total_pages }} 页</span></li>
                    </ul>
                </nav>
            </div>
        </div>
        <aside class="sidebar">
            <div class="fixed">
                <div class="widget widget_hot">
                    <div>{% include tag.cloud.md %}</div>
                </div>
                <div class="widget widget_sentence">
                    <h3>友情链接</h3>
                    <div class="widget-sentence-link">
                        <div>&raquo; <a href="http://bakerstreet.club" target="_blank" title="۩ 贝克街俱乐部">۩ 贝克街俱乐部</a>
                        </div>
                        <div>&raquo; <a href="http://sherlock.help" target="_blank" title="☎ 呼叫夏洛克">☎ 呼叫夏洛克</a> </div>
                        <div>&raquo; <a href="http://feels.tech" target="_blank" title="♈ 感之科技">♈ 感之科技</a> </div>
                        <div>&raquo; <a href="http://gogoogle.top" target="_blank" title="ஐ 上！谷歌之巅！！">ஐ 上！谷歌之巅！！</a>
                        </div>
                        <div style="padding:30px 0"></div>
                    </div>
                </div>
            </div>
        </aside>
    </section>
</div>