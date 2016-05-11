# [Markdown](http://baike.baidu.com/link?url=W5NIUf4fJnG8H_H_xRnxlFkYm17m-KX1zxoJZ4YLozH1VIM6_Si-r6VAV5pClC9ge1aePiGduNYCGlGlkRDXba) 简单使用

## 目录

* [标题] (#headers)
* [列表] (#list)
* [区块引用] (#Blockquotes)
* [分割线] (#cutting-line)
* [强调] (#Emphasis)
* [代码] (#code)
* [图片] (#img)

<a name="headers">
</a>
### 标题

    # 一级标题
    #### 四级标题

一级和二级标题还有一种写法：

    一级标题
    ===================
    二级标题
    --------------------

<a name="list">
</a>
### 列表

* 无需列表(* 或者+ ，- )
    * listitem1
    * listitem2

* 有序列表(数字接着一个英文句点)
    1. Bird
    2. McHale
    3. Parish

    <a name="Blockquotes">
    </a>
### 区块引用(>)

>This is a blockquote with two paragraphs. Lorem ipsum dolor sit amet,
>> consectetuer adipiscing elit. Aliquam hendrerit mi posuere lectus.


<a name="cutting-line">
</a>
### 分割线
你可以在一行中用三个以上的星号、减号、底线来建立一个分隔线，行内不能有其他东西。你也可以在星号或是减号中间插入空格。下面每种写法都可以建立分隔线：
    ***
    * * *
    - - -
    ------

<a name="link">
</a>
### 链接
Markdown 支持两种形式的链接语法： 行内式和参考式两种形式。

不管是哪一种，链接文字都是用 [方括号] 来标记。

要建立一个行内式的链接，只要在方块括号后面紧接着圆括号并插入网址链接即可，如果你还想要加上链接的 title 文字，只要在网址后面，用双引号把 title 文字包起来即可，例如：

     This is [an example](http://example.com/ "Title") inline link.
     [This link](http://example.net/) has no title attribute.

如果你是要链接到同样主机的资源，你可以使用相对路径：

     See my [About](/about/) page for details.
参考式的链接是在链接文字的括号后面再接上另一个方括号，而在第二个方括号里面要填入用以辨识链接的标记：

     This is [an example][id] reference-style link.
你也可以选择性地在两个方括号中间加上一个空格：

     This is [an example] [id] reference-style link.
接着，在文件的任意处，你可以把这个标记的链接内容定义出来：

     [id]: http://example.com/  "Optional Title Here"

链接内容定义的形式为：
     *  方括号（前面可以选择性地加上至多三个空格来缩进），里面输入链接文字
     * 接着一个冒号
     * 接着一个以上的空格或制表符
     * 接着链接的网址
     * 选择性地接着 title 内容，可以用单引号、双引号或是括弧包着
     下面这三种链接的定义都是相同：

     [foo]: http://example.com/  "Optional Title Here"
     [foo]: http://example.com/  'Optional Title Here'
     [foo]: http://example.com/  (Optional Title Here)

网址定义只有在产生链接的时候用到，并不会直接出现在文件之中。

     [link text][a]
     [link text][A]
隐式链接标记功能让你可以省略指定链接标记，这种情形下，链接标记会视为等同于链接文字，要用隐式链接标记只要在链接文字后面加上一个空的方括号，如果你要让 "Google" 链接到 google.com，你可以简化成：

     [Google][]
然后定义链接内容：

     [Google]: http://google.com/
由于链接文字可能包含空白，所以这种简化型的标记内也许包含多个单词：

     Visit [Daring Fireball][] for more information.
然后接着定义链接：

     [Daring Fireball]: http://daringfireball.net/
链接的定义可以放在文件中的任何一个地方，我比较偏好直接放在链接出现段落的后面，你也可以把它放在文件最后面，就像是注解一样。
下面是一个参考式链接的范例：

      I get 10 times more traffic from [Google] [1] than from
     [Yahoo] [2] or [MSN] [3].

       [1]: http://google.com/        "Google"
       [2]: http://search.yahoo.com/  "Yahoo Search"
       [3]: http://search.msn.com/    "MSN Search"
     如果改成用链接名称的方式写：

     I get 10 times more traffic from [Google][] than from
     [Yahoo][] or [MSN][].

       [google]: http://google.com/        "Google"
       [yahoo]:  http://search.yahoo.com/  "Yahoo Search"
       [msn]:    http://search.msn.com/    "MSN Search"
上面两种写法都会产生下面的 HTML。

     <p>I get 10 times more traffic from <a href="http://google.com/"
     title="Google">Google</a> than from
     <a href="http://search.yahoo.com/" title="Yahoo Search">Yahoo</a>
     or <a href="http://search.msn.com/" title="MSN Search">MSN</a>.</p>
     下面是用行内式写的同样一段内容的 Markdown 文件，提供作为比较之用：

     I get 10 times more traffic from [Google](http://google.com/ "Google")
     than from [Yahoo](http://search.yahoo.com/ "Yahoo Search") or
     [MSN](http://search.msn.com/ "MSN Search").
参考式的链接其实重点不在于它比较好写，而是它比较好读，比较一下上面的范例，使用参考式的文章本身只有 81 个字符，但是用行内形式的却会增加到 176 个字元，如果是用纯 HTML 格式来写，会有 234 个字元，在 HTML 格式中，标签比文本还要多。
使用 Markdown 的参考式链接，可以让文件更像是浏览器最后产生的结果，让你可以把一些标记相关的元数据移到段落文字之外，你就可以增加链接而不让文章的阅读感觉被打断。

<a name="Emphasis">
</a>
### 强调
Markdown 使用星号（*）和底线（_）作为标记强调字词的符号，被 * 或 _ 包围的字词会被转成用 <em> 标签包围，用两个 * 或 _ 包起来的话，则会被转成 <strong>，例如：

     *single asterisks*

     _single underscores_

     **double asterisks**

     __double underscores__

如果要在文字前后直接插入普通的星号或底线，你可以用反斜线：

     \*this text is surrounded by literal asterisks\*

<a name="code">
</a>
###代码

如果要标记一小段行内代码，你可以用反引号把它包起来(`)，例如：

    Use the `printf()` function.

<a name="img">
</a>
###图片

很明显地，要在纯文字应用中设计一个「自然」的语法来插入图片是有一定难度的。
Markdown 使用一种和链接很相似的语法来标记图片，同样也允许两种样式： 行内式和参考式。
行内式的图片语法看起来像是：
    ![Alt text](/path/to/img.jpg)
    ![Alt text](/path/to/img.jpg "Optional title")
详细叙述如下：
一个惊叹号 !
接着一个方括号，里面放上图片的替代文字
接着一个普通括号，里面放上图片的网址，最后还可以用引号包住并加上 选择性的 'title' 文字。
参考式的图片语法则长得像这样：

     ![Alt text][id]
「id」是图片参考的名称，图片参考的定义方式则和连结参考一样：

     [id]: url/to/image  "Optional title attribute"
