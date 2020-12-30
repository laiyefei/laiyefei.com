<h3  style="text-shadow: 0 0 3px {{ include.titleColor }}" >{{ include.title }}</h3>
<div class="widget-sentence-content">  
   <ul class="plinks ptags" id="ulTagWall">           
        {% for group in include.groups %}
        <li style="width:108px">
            <a href="#{{ group | first }}" times="1" onclick="javascript:tagDoAutoHide('{{ group | first }}', this);" title="{{ group | first }}" >
        <div style="position:relative;">
            <span style="
            background-color:#eee;
            display: inline-block;
            overflow: hidden;
            text-overflow:ellipsis;
            white-space: nowrap;
            width:calc(100% - 10px);
            float:left;
            letter-spacing: 1px;
            text-align: right;
            font-size: 12px;
            " >
            {{ group | first }}
            </span>
            <span style="float:right;width:10px;background-color:#eee;color:#c166b1;padding-left:2px;font-weight: bold;font-size:20px;"><sup>{{ group | last | size }}</sup></span>
        </div>
        </a></li>
        {% endfor %} 
    </ul>
</div>