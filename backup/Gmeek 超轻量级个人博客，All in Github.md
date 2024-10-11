Gmeek快速上手
=========

[](https://blog.meekdai.com/ "首页")[](https://github.com/Meekdai/meekdai.github.io/issues/39 "Issue")[](https://blog.meekdai.com/post/Gmeek-kuai-su-shang-shou.html "切换主题")

[Gmeek](https://github.com/Meekdai/Gmeek) 一个博客框架，超轻量级个人博客模板，完全基于`Github Pages` 、 `Github Issues` 和 `Github Actions`，可以称作`All in Github`。不需要本地部署，从搭建到写作，只需要18秒，2步搭建好博客，第3步就是写作。

一、安装
----

Important

安装及其简单，但是也要认真看下面的步骤，一步一步来。

1.  【创建仓库】点击[通过模板创建仓库](https://github.com/new?template_name=Gmeek-template&template_owner=Meekdai)，建议仓库名称为`XXX.github.io`，其中`XXX`为你的github用户名。
    
2.  【启用Pages】在仓库的设置`Settings`中`Pages->Build and deployment->Source`下面选择`Github Actions`。
    
3.  【开始写作】打开一篇issue，开始写作，并且**必须**添加一个`标签Label`（至少添加一个），再保存issue后会自动创建博客内容，片刻后可通过[https://XXX.github.io](https://xxx.github.io/) 访问（可进入Actions页面查看构建进度）。
    
4.  【手动全局生成】这个步骤只有在修改`config.json` 文件或者出现奇怪问题的时候，需要执行。
    

```p4
通过Actions->build Gmeek->Run workflow->里面的按钮全局重新生成一次
```

Note

网友制作的视频教程：[https://www.bilibili.com/video/BV1GM4m1m7ZD/](https://www.bilibili.com/video/BV1GM4m1m7ZD/)

二、配置文件
------

Tip

按照安装步骤成功搭建好后，就可以阅读下面的内容修改配置文件啦。  
注意修改配置文件后一定要手动全局生成一次，不然会报错。  
如果对`json`格式不熟悉，建议先简单学习一下。

`config.json` 文件就是配置文件，在创建的仓库内可以找到，对应修改为自己的即可。

```js
{
    "title":"Meekdai",
    "subTitle":"童话是一种生活态度，仅此而已。",
    "avatarUrl":"https://github.githubassets.com/favicons/favicon.svg",
    "GMEEK_VERSION":"last"
}
```

以上是必须的字段，下面是可以自定义字段的描述，可以选择加入到`config.json`中。

```js
"displayTitle":"Meekdai",
"homeUrl":"http://blog.meekdai.com",
"faviconUrl":"https://github.githubassets.com/favicons/favicon.svg",
"email":"meekdai@163.com",
"startSite":"02/16/2015",
"filingNum":"浙ICP备20023628号",
"onePageListNum":15,
"singlePage":["about"],
"iconList":{"music":"M0 8a8 8 0 1 1 16 0A8 8 0 0 1 0 8Zm8-6.5a6.5 6.5 0 1 0 0 13 6.5 6.5 0 0 0 0-13Z"},
"exlink":{"music":"https://music.meekdai.com"},
"commentLabelColor":"#006b75",
"yearColorList":["#bc4c00", "#0969da", "#1f883d", "#A333D0"],
"i18n":"CN",
"UTC":8,
"themeMode":"manual",
"dayTheme":"light",
"nightTheme":"dark_colorblind",
"urlMode":"pinyin",
"style":"",
"script":"",
"head":"",
"allHead":"",
"indexStyle":"",
"indexScript":"",
"showPostSource":1,
"rssSplit":"sentence",
"bottomText":"转载请注明出处",
"ogImage":"https://cdn.jsdelivr.net/gh/Meekdai/meekdai.github.io/logo64.jpg",
"primerCSS":"<link href='https://mirrors.sustech.edu.cn/cdnjs/ajax/libs/Primer/21.0.7/primer.css' rel='stylesheet' />",
"needComment":0,
```

Caution

最后一行配置末尾不需要逗号，其他行末尾都需要逗号（英文逗号）

| **配置参数** | **说明** |
| --- | --- |
| title | 【必填】博客标题 |
| subTitle | 【必填】博客描述&自述 |
| avatarUrl | 【必填】博客头像 |
| GMEEK\_VERSION | 【必填】Gmeek版本，一般写`last`也可以用具体tag版本 |
| displayTitle | 用于头像后面的标题展示，如果和`title`一致则不用添加 |
| homeUrl | 博客的主页地址，自定义域名时需要配置 |
| faviconUrl | 页面的favicon地址，如果和avatarUrl一致则不用添加 |
| email | 用于自动提交仓库时用，不添加也可以 |
| startSite | 用于页面底部显示网站运行天数 |
| filingNum | 用于页面底部显示备案信息 |
| onePageListNum | 用于首页每页展示的文章数量 |
| singlePage | 自定义独立页面，例如`about`或者`link`等 |
| iconList | 用于定义singlePage按钮展示的[SVG图标](https://primer.style/foundations/icons/#16px) (16px)，`about`和`link`内置无需定义 |
| exlink | 用于自定义首页右上角圆形按钮到外部链接功能，按钮图标定义在iconList中 |
| commentLabelColor | 用于自定义显示评论数量标签的颜色 |
| yearColorList | 用于自定义显示不同年份标签的颜色 |
| i18n | 用于定义博客语言，目前支持`EN`/`CN`/`RU` |
| UTC | 用于定义[时区](https://en.wikipedia.org/wiki/List_of_UTC_offsets) |
| themeMode | 用于定义主题模式，默认为`manual`，也可选择`fix`[详细说明](https://blog.meekdai.com/post/%E3%80%90Gmeek-jin-jie-%E3%80%91-liang-an-zhu-ti-pei-zhi-fang-shi.html) |
| dayTheme | 用于定义[亮主题](https://github.com/settings/appearance) |
| nightTheme | 用于定义[暗主题](https://github.com/settings/appearance) |
| urlMode | 用于定义文章链接生成模式，目前支持`pinyin`/`issue`/`ru_translit` |
| style | 用于自定义文章页CSS |
| script | 用于自定义文章页JavaScript |
| head | 用于自定义文章页head内容 |
| allHead | 用于自定义所有页面head内容 |
| indexStyle | 用于自定义首页CSS |
| indexScript | 用于自定义首页JavaScript |
| showPostSource | 设置为1则在文章页显示issue链接按钮，设置为0则不显示 |
| rssSplit | 设置RSS输出的截断符号，默认`sentence`为第一句话，可配置其他特殊符号 |
| bottomText | 用于设置文章页面右下角显示的内容 |
| ogImage | 用于设置Open Graph协议展示的图片 |
| primerCSS | 用于设置primer.css的CDN地址，默认使用[南科大](https://mirrors.sustech.edu.cn/cdnjs/ajax/libs/Primer/21.0.7/primer.css) |
| needComment | 用于设置是否需要评论功能，1开启评论，0关闭 |

三、常见问题
------

### 1\. 搭建不成功

多半是没有按照安装步骤来，其实搭建就这2步，不要自己乱点乱设置，就不会有问题。

*   案例一：[Meekdai/Gmeek#14](https://github.com/Meekdai/Gmeek/issues/14)
*   案例二：[Meekdai/Gmeek#18](https://github.com/Meekdai/Gmeek/issues/18)
*   案例二：[Meekdai/Gmeek#20](https://github.com/Meekdai/Gmeek/issues/20)

### 2\. Actions执行失败

修改了`config.json`配置文件后，需要全局生成。另外`label`标签没有打会出现这个问题。  
建议通过Actions->build Gmeek->Run workflow->里面的按钮全局重新生成一次

*   案例一：[Meekdai/Gmeek#1](https://github.com/Meekdai/Gmeek/issues/1)
*   案例二：[Meekdai/Gmeek#10](https://github.com/Meekdai/Gmeek/issues/10)

### 3\. 导入以前的文章

如需修改发布时间，可以在文章最后一行添加如下代码。里面的时间是采用时间戳的形式，可以用如下[网站](https://tool.lu/timestamp)转换。

```html
<!-- ##{"timestamp":1490764800}## -->
```

### 4\. 自定义单篇文章参数

自定义单篇文章页面的`style`和`script`

```html
<!-- ##{"style":"<style>#postBody{font-size:20px}</style>"}## -->
```

```html
<!-- ##{"script":"<script async src='//busuanzi.ibruce.info/busuanzi/2.3/busuanzi.pure.mini.js'></script>"}## -->
```

### 5\. 多种自定义参数

可同时一起添加多种自定义参数：

```html
<!-- ##{"script":"<script async src='//busuanzi.ibruce.info/busuanzi/2.3/busuanzi.pure.mini.js'></script>","style":"<style>#postBody{font-size:20px}</style>","timestamp":1490764800}## -->
```

### 6\. 自定义全局文章参数

添加全局文章页面的`style`和`script`，在`config.json`文件中添加

```js
"style":"<style>#postBody{font-size:20px}</style>",
"script":"<script async src='//busuanzi.ibruce.info/busuanzi/2.3/busuanzi.pure.mini.js'></script>",
```

### 7\. 置顶博客文章

只需要`Pin issue`后，手动全局生成一次即可。

### 8\. utteranc报错

如果在评论里面登录后评论报错，可直接按照提示安装`utteranc app`即可

```
Error: utterances is not installed on xxx/xxx.github.io. If you own this repo, install the app. Read more about this change in the PR.

```

### 9\. 删除文章

只需要`Close issue`或者`Delete issue`后，再手动全局生成一次即可。

四、进阶教程
------

Gmeek的可定制化功能非常高，下面的链接是一些更加高级的设置教程，还有插件的使用等。  
[https://meekdai.github.io/tag.html#Gmeek](https://meekdai.github.io/tag.html#Gmeek)

❤️ 转载文章请注明出处，谢谢！❤️

评论

Copyright © [Meekdai](https://blog.meekdai.com/)

Powered by [Gmeek](https://meekdai.com/Gmeek.html)

var now=new Date(); document.getElementById("copyrightYear").innerHTML=now.getFullYear(); if("02/16/2015"!=""){ var startSite=new Date("02/16/2015"); var diff=now.getTime()-startSite.getTime(); var diffDay=Math.floor(diff/(1000\*60\*60\*24)); document.getElementById("runday").innerHTML="网站运行"+diffDay+"天"+" • "; }

var IconList={'sun': 'M8 10.5a2.5 2.5 0 100-5 2.5 2.5 0 000 5zM8 12a4 4 0 100-8 4 4 0 000 8zM8 0a.75.75 0 01.75.75v1.5a.75.75 0 01-1.5 0V.75A.75.75 0 018 0zm0 13a.75.75 0 01.75.75v1.5a.75.75 0 01-1.5 0v-1.5A.75.75 0 018 13zM2.343 2.343a.75.75 0 011.061 0l1.06 1.061a.75.75 0 01-1.06 1.06l-1.06-1.06a.75.75 0 010-1.06zm9.193 9.193a.75.75 0 011.06 0l1.061 1.06a.75.75 0 01-1.06 1.061l-1.061-1.06a.75.75 0 010-1.061zM16 8a.75.75 0 01-.75.75h-1.5a.75.75 0 010-1.5h1.5A.75.75 0 0116 8zM3 8a.75.75 0 01-.75.75H.75a.75.75 0 010-1.5h1.5A.75.75 0 013 8zm10.657-5.657a.75.75 0 010 1.061l-1.061 1.06a.75.75 0 11-1.06-1.06l1.06-1.06a.75.75 0 011.06 0zm-9.193 9.193a.75.75 0 010 1.06l-1.06 1.061a.75.75 0 11-1.061-1.06l1.06-1.061a.75.75 0 011.061 0z', 'moon': 'M9.598 1.591a.75.75 0 01.785-.175 7 7 0 11-8.967 8.967.75.75 0 01.961-.96 5.5 5.5 0 007.046-7.046.75.75 0 01.175-.786zm1.616 1.945a7 7 0 01-7.678 7.678 5.5 5.5 0 107.678-7.678z', 'sync': 'M1.705 8.005a.75.75 0 0 1 .834.656 5.5 5.5 0 0 0 9.592 2.97l-1.204-1.204a.25.25 0 0 1 .177-.427h3.646a.25.25 0 0 1 .25.25v3.646a.25.25 0 0 1-.427.177l-1.38-1.38A7.002 7.002 0 0 1 1.05 8.84a.75.75 0 0 1 .656-.834ZM8 2.5a5.487 5.487 0 0 0-4.131 1.869l1.204 1.204A.25.25 0 0 1 4.896 6H1.25A.25.25 0 0 1 1 5.75V2.104a.25.25 0 0 1 .427-.177l1.38 1.38A7.002 7.002 0 0 1 14.95 7.16a.75.75 0 0 1-1.49.178A5.5 5.5 0 0 0 8 2.5Z', 'home': 'M6.906.664a1.749 1.749 0 0 1 2.187 0l5.25 4.2c.415.332.657.835.657 1.367v7.019A1.75 1.75 0 0 1 13.25 15h-3.5a.75.75 0 0 1-.75-.75V9H7v5.25a.75.75 0 0 1-.75.75h-3.5A1.75 1.75 0 0 1 1 13.25V6.23c0-.531.242-1.034.657-1.366l5.25-4.2Zm1.25 1.171a.25.25 0 0 0-.312 0l-5.25 4.2a.25.25 0 0 0-.094.196v7.019c0 .138.112.25.25.25H5.5V8.25a.75.75 0 0 1 .75-.75h3.5a.75.75 0 0 1 .75.75v5.25h2.75a.25.25 0 0 0 .25-.25V6.23a.25.25 0 0 0-.094-.195Z', 'github': 'M8 0c4.42 0 8 3.58 8 8a8.013 8.013 0 0 1-5.45 7.59c-.4.08-.55-.17-.55-.38 0-.27.01-1.13.01-2.2 0-.75-.25-1.23-.54-1.48 1.78-.2 3.65-.88 3.65-3.95 0-.88-.31-1.59-.82-2.15.08-.2.36-1.02-.08-2.12 0 0-.67-.22-2.2.82-.64-.18-1.32-.27-2-.27-.68 0-1.36.09-2 .27-1.53-1.03-2.2-.82-2.2-.82-.44 1.1-.16 1.92-.08 2.12-.51.56-.82 1.28-.82 2.15 0 3.06 1.86 3.75 3.64 3.95-.23.2-.44.55-.51 1.07-.46.21-1.61.55-2.33-.66-.15-.24-.6-.83-1.23-.82-.67.01-.27.38.01.53.34.19.73.9.82 1.13.16.45.68 1.31 2.69.94 0 .67.01 1.3.01 1.49 0 .21-.15.45-.55.38A7.995 7.995 0 0 1 0 8c0-4.42 3.58-8 8-8Z', 'copy': 'M0 6.75C0 5.784.784 5 1.75 5h1.5a.75.75 0 0 1 0 1.5h-1.5a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-1.5a.75.75 0 0 1 1.5 0v1.5A1.75 1.75 0 0 1 9.25 16h-7.5A1.75 1.75 0 0 1 0 14.25Z M5 1.75C5 .784 5.784 0 6.75 0h7.5C15.216 0 16 .784 16 1.75v7.5A1.75 1.75 0 0 1 14.25 11h-7.5A1.75 1.75 0 0 1 5 9.25Zm1.75-.25a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-7.5a.25.25 0 0 0-.25-.25Z', 'check': 'M13.78 4.22a.75.75 0 0 1 0 1.06l-7.25 7.25a.75.75 0 0 1-1.06 0L2.22 9.28a.751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018L6 10.94l6.72-6.72a.75.75 0 0 1 1.06 0Z'}; var utterancesLoad=0; let themeSettings={ "dark": \["dark","moon","#00f0ff","dark-blue"\], "light": \["light","sun","#ff5000","github-light"\], "auto": \["auto","sync","","preferred-color-scheme"\] }; function changeTheme(mode, icon, color, utheme){ document.documentElement.setAttribute("data-color-mode",mode); document.getElementById("themeSwitch").setAttribute("d",value=IconList\[icon\]); document.getElementById("themeSwitch").parentNode.style.color=color; if(utterancesLoad==1){utterancesTheme(utheme);} } function modeSwitch(){ let currentMode=document.documentElement.getAttribute('data-color-mode'); let newMode = currentMode === "light" ? "dark" : currentMode === "dark" ? "auto" : "light"; localStorage.setItem("meek\_theme", newMode); if(themeSettings\[newMode\]){ changeTheme(...themeSettings\[newMode\]); } } function utterancesTheme(theme){ const message={type:'set-theme',theme: theme}; const iframe=document.getElementsByClassName('utterances-frame')\[0\]; iframe.contentWindow.postMessage(message,'https://utteranc.es'); } if(themeSettings\[theme\]){changeTheme(...themeSettings\[theme\]);} console.log("\\n %c Gmeek main https://github.com/Meekdai/Gmeek \\n","padding:5px 0;background:#02d81d;color:#fff"); document.getElementById("pathHome").setAttribute("d",IconList\["home"\]); document.getElementById("pathIssue").setAttribute("d",IconList\["github"\]); cmButton=document.getElementById("cmButton"); span=document.createElement("span"); span.setAttribute("class","Counter"); span.innerHTML="124"; cmButton.appendChild(span); function openComments(){ cm=document.getElementById("comments"); cmButton=document.getElementById("cmButton"); cmButton.innerHTML="loading"; span=document.createElement("span"); span.setAttribute("class","AnimatedEllipsis"); cmButton.appendChild(span); script=document.createElement("script"); script.setAttribute("src","https://utteranc.es/client.js"); script.setAttribute("repo","Meekdai/meekdai.github.io"); script.setAttribute("issue-term","title"); if(localStorage.getItem("meek\_theme")=="dark"){script.setAttribute("theme","dark-blue");} else if(localStorage.getItem("meek\_theme")=="light") {script.setAttribute("theme","github-light");} else{script.setAttribute("theme","preferred-color-scheme");} script.setAttribute("crossorigin","anonymous"); script.setAttribute("async",""); cm.appendChild(script); int=self.setInterval("iFrameLoading()",200); } function iFrameLoading(){ var utterances=document.getElementsByClassName('utterances'); if(utterances.length==1){ if(utterances\[0\].style.height!=""){ utterancesLoad=1; int=window.clearInterval(int); document.getElementById("cmButton").style.display="none"; console.log("utterances Load OK"); } } } document.addEventListener('DOMContentLoaded', () => { const createClipboardHTML = (codeContent, additionalClasses = '') => \` <pre class="notranslate"><code class="notranslate">${codeContent}</code></pre> <div class="clipboard-container position-absolute right-0 top-0 ${additionalClasses}"> <clipboard-copy class="ClipboardButton btn m-2 p-0" role="button" style="display: inherit;"> <svg height="16" width="16" class="octicon octicon-copy m-2"><path d="${IconList\["copy"\]}"></path></svg> <svg height="16" width="16" class="octicon octicon-check color-fg-success m-2 d-none"><path d="${IconList\["check"\]}"></path></svg> </clipboard-copy> <div class="copy-feedback">Copied!</div> </div> \`; const handleCodeElements = (selector = '') => { document.querySelectorAll(selector).forEach(codeElement => { const codeContent = codeElement.innerHTML; const newStructure = document.createElement('div'); newStructure.className = 'snippet-clipboard-content position-relative overflow-auto'; newStructure.innerHTML = createClipboardHTML(codeContent); const parentElement = codeElement.parentElement; if (selector.includes('highlight')) { parentElement.insertBefore(newStructure, codeElement.nextSibling); parentElement.removeChild(codeElement); } else { parentElement.parentElement.replaceChild(newStructure, parentElement); } }); }; handleCodeElements('pre.notranslate > code.notranslate'); handleCodeElements('div.highlight > pre.notranslate'); let currentFeedback = null; document.querySelectorAll('clipboard-copy').forEach(copyButton => { copyButton.addEventListener('click', () => { const codeContent = copyButton.closest('.snippet-clipboard-content').innerText; const tempTextArea = document.createElement('textarea'); tempTextArea.value = codeContent; document.body.appendChild(tempTextArea); tempTextArea.select(); document.execCommand('copy'); document.body.removeChild(tempTextArea); const copyIcon = copyButton.querySelector('.octicon-copy'); const checkIcon = copyButton.querySelector('.octicon-check'); const copyFeedback = copyButton.nextElementSibling; if (currentFeedback && currentFeedback !== copyFeedback) {currentFeedback.style.display = 'none';} currentFeedback = copyFeedback; copyIcon.classList.add('d-none'); checkIcon.classList.remove('d-none'); copyFeedback.style.display = 'block'; copyButton.style.borderColor = 'var(--color-success-fg)'; setTimeout(() => { copyIcon.classList.remove('d-none'); checkIcon.classList.add('d-none'); copyFeedback.style.display = 'none'; copyButton.style.borderColor = ''; }, 2000); }); }); });

  

本文转自 [https://blog.meekdai.com/post/Gmeek-kuai-su-shang-shou.html](https://blog.meekdai.com/post/Gmeek-kuai-su-shang-shou.html)，如有侵权，请联系删除。