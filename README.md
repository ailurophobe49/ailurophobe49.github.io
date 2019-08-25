## 项目主目录
- index.html为项目首页
    ```
        ---
        layout: default
        title: 我的Blog
        ---
        <h2>{{ page.title }}</h2>
        <p>最新文章</p>
        <ul>
        　　{% for post in site.posts %} //对所有帖子进行一个遍历（输出内容使用两层大括号，单纯的命令使用一层大括号）
        　　　　<li>{{ post.date | date_to_string }} <a href="{{ site.baseurl }}{{ post.url }}">{{ post.title }}</a></li>
        　　{% endfor %}
        </ul>
    ```

- _config.yml	
    + 保存配置数据。很多配置选项都会直接从命令行中进行设置，但是如果你把那些配置写在这儿，你就不用非要去记住那些命令了。
- _drafts	
    + drafts 是未发布的文章。这些文件的格式中都没有 title.MARKUP 数据。学习如何使用 drafts.
- _includes	
    + 你可以加载这些包含部分到你的布局或者文章中以方便重用。可以用这个标签 {% include file.ext %} 来把文件 _includes/file.ext 包含进来。
- _layouts	
    + layouts 是包裹在文章外部的模板。布局可以在 YAML 头信息中根据不同文章进行选择。 这将在下一个部分进行介绍。标签 {{ content }} 可以将content插入页面中。
- _posts	
    + 这里放的就是你的文章了。文件格式很重要，必须要符合: YEAR-MONTH-DAY-title.MARKUP。 The permalinks 可以在文章中自己定制，但是数据和标记语言都是根据文件名来确定的。
- _data	
    + 放一些其他配置文件,必须是.yml或者.yaml格式的,比如有一个文件叫members.yml,如果想引用这个文件里的内容就通过site.data.membres来引用
- _site	
    + 一旦 Jekyll 完成转换，就会将生成的页面放在这里（默认）。最好将这个目录放进你的 .gitignore 文件中。
