# Vim Script 文档中文计划 #
Vim Script 即 Vim 脚本，又称 Vim 插件(Plugin)，以下统称“脚本”。

这是个业余的兴趣项目，主要是由各个成员翻译自己熟悉、推荐的优秀脚本介绍（并附上一些小技巧之类），同样还会尽力翻译对应脚本的帮助文档。

欢迎有兴趣的朋友加入翻译或推荐脚本。参加方法：(建议使用自己的Gmail) 发邮件到 hotoo.cn![http://vim-script-cn.googlecode.com/svn/trunk/img/at.png](http://vim-script-cn.googlecode.com/svn/trunk/img/at.png)gmail.com

# 广告：[欢迎加入 Vim 的 Gtalk 群](http://hotoo.googlecode.com/svn/blog/Gtalk-group-for-Vim.html) #

![http://vim-script-cn.googlecode.com/svn/trunk/img/vim-logo.png](http://vim-script-cn.googlecode.com/svn/trunk/img/vim-logo.png)


## 0. 预览 ##
  * [帮助文档](http://code.google.com/p/vim-script-cn/source/browse/#svn/trunk/doc)
  * [官方介绍](http://vim-script-cn.googlecode.com/svn/trunk/intro/index.html)
  * [Vim 资料收集](https://dl.dropbox.com/u/1151037/vimwiki/Vim.html)
  * 翻译计划：[PLAN](PLAN.md)


## 1. 翻译方法及约定 ##

### 1.1. 帮助文档 ###
注：使用文档：即脚本附带的使用说明，一般要放置到 vimfiles/doc 目录中。
  * 翻译的文件与原始文档同名，后缀改为 .cnx
  * 文件放置到 trunk/doc/ 目录中。
  * 翻译完成后，在 Vim 中执行一下命令生成 tag：
> Windows:
```
  :helptags $VIM/vimfiles/doc
```
> Linux:
```
  :helptags ~/.vim/doc
```

### 1.2. 官方主页 ###
[Vim Script 官方主页](http://www.vim.org/scripts/index.php)

方法 I: 使用 Vimwiki (**推荐**)。
  1. 确认正确安装了 [Vimwiki](http://www.vim.org/scripts/script.php?script_id=2226) 脚本。
  1. 将 [vimwiki.snippets](http://vim-script-cn.googlecode.com/svn/trunk/intro-wiki/template/vimwiki.snippets) 放置到 vimfiles/snippets 目录中。
  1. 因为 Vimwiki 和 snipMate 的 < Tab> 热键冲突，可以将 vimfiles/ftplugin/vimwiki.vim 中第 293 行 的
```
  inoremap <expr> <buffer> <Tab> vimwiki_tbl#kbd_tab()
```
> > 换成另外的热键，例如：
```
inoremap <expr> <buffer> <C-Tab> vimwiki_tbl#kbd_tab()
```
  1. 到此，在 .wiki 文件中输入 wiki< Tab> 或 template< Tab> 就可以完成模板，另有其他一些简单的模板，自己也可以补充。
  1. 在 vimrc 的 ·g:vimwiki\_list· 中加入一个 wiki 。例如我的：
```
let g:vimwiki_list = [{'path': 'D:\My Dropbox\VimPrivateWiki'},
                    \ {'path': 'D:\My Dropbox\vimwiki',
                    \ 'path_html': 'D:\My Dropbox\Public\vimwiki',
                    \ 'html_header': 'D:\My Dropbox\vimwiki\template\header.tpl',
                    \ 'html_footer': 'D:\My Dropbox\vimwiki\template\footer.tpl'},
                    \ {'path': 'F:\vim-script-cn\intro-wiki',
                    \ 'path_html': 'F:\vim-script-cn\intro',
                    \ 'html_header': 'F:\vim-script-cn\intro-wiki\template\header.tpl',
                    \ 'html_footer': 'F:\vim-script-cn\intro-wiki\template\footer.tpl'}
                    \ ]
```

> 重启 Vim ，按 3< leader>ww (一般是 3\ww , 3 是指Vimwiki列表中第3个wiki) 即可快速启动 Vim 脚本 文档中文计划的 wiki 首页。


WikiWord 命名规则：
```
"script_" + SCRIPT_ID + "_" + SCRIPT_NAME + "|" + SCRIPT_NAME
```
例如：
```
[[script_2226_Vimwiki|Vimwiki]]
```


方法 II: 写 HTML。
  * 主要使用这个 [模板](http://vim-script-cn.googlecode.com/svn/trunk/intro/template.html)。
  * “create by” 翻译为 “作者”
  * “description”翻译为 “描述”
  * “install details”翻译为“安装细节”
  * 每段均放在 < p> 标签中；内嵌在翻译文本中的小段代码放在 < code> 中；大段或换行的代码放在 < pre class="code"> 中。
  * 提交html文档时，给文档添加如下svn属性：svn:mime-type，值为 text/html
  * 插件帮助文档需在最后加上模式行，指定为帮助文件类型


方法 III: 直接使用纯文本：
  * 使用电子邮件，将翻译好的内容和相关信息(包括被翻译的URL地址) 发送到 hotoo.cn![http://vim-script-cn.googlecode.com/svn/trunk/img/at.png](http://vim-script-cn.googlecode.com/svn/trunk/img/at.png)gmail.com


## 2. 分工 ##
  * 建议每个脚本的文档由一人独立完成；
  * 对于需要多人合作的大文档，建议由参与者商讨分工，完成后相互review、合并文档。