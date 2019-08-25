## 我的文章
- 文章就是普通的文本文件，文件名假定为2018-06-11-hello world.html。(注意，文件名必须为"年-月-日-文章标题.后缀名"的格式。如果网页代码采用html格式，后缀名为html；如果采用markdown格式，后缀名为md）在该文件中，填入以下内容：
    ```
        ---              //每篇文章开头必须有一个yaml文件头，用三根短划线"---"来标记开始和结束，里面每一行设置一种元素
        layout: default  //该文章的模板使用_layouts目录下的default.html文件 
        title: 你好，世界 //该文章的标题是"你好，世界"（如果不设置这个值，默认使用嵌入文件名的标题，即"hello world"）
        ---  
        <h2>{{ page.title }}</h2> //{{ page.title }}就是文件头中设置的"你好，世界"
        <p>我的第一篇文章</p>
        <p>{{ page.date | date_to_string }}</p> //{{ page.date }}是嵌入文件名的日期，"| date_to_string"表示将page.date变量转化成人类可读的格式。
    ```