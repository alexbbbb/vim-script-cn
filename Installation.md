# 安装 Vim Script 中文文档 #
  1. 下载 [Vim script 中文文档(\*.cnx)](http://code.google.com/p/vim-script-cn/source/browse/#svn/trunk/doc)
  1. 放至 Vim 用户目录下的 doc 目录中<br />
> > for Windows: `$VIM/vimfiles/doc`<br />
> > for Linux &　Mac: `~/.vim/doc`<br />
> > 以下统称 $VIM/vimfiles 和 ~/.vim 目录为 runtime 目录。
  1. 在 Vim 环境中运行 `helptags` 命令：
> > for Windows:
```
    :helptags $Vim/vimfiles/doc
```
> > for Linux & Mac:
```
    :helptags ~/.vim/doc
```
  1. 此时文档的 tags 已生成。
  1. 设置 Vim 使用的文档语言，默认是英文。
```
    :set helplang=cn
```
> > 如果在 vimrc 设置无效，可以查看并修改 runtime/plugin/vimcdoc.vim 中的设置，之前安装有 Vim 中文帮助则可以忽略这步。