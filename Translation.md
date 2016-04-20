# Vim Script 翻译方法及技巧说明 #

## 1. checkout ##
建议大家从 https://vim-script-cn.googlecode.com/svn/ 开始 checkout，而不是
项目默认提供的 https://vim-script-cn.googlecode.com/svn/trunk/ ，
这样就可以把包括 branches, tags, trunk, wiki 几个目录都 checkout 下来。

trunk/doc 目录下均只存放被翻译的 .cnx 文档，一般来说，
大家在 trunk 下直接翻译就好了，无需打分支到 branches 下，当然打分支同样也可以。

## 2. 翻译 ##
  1. 在 .cnx 文档的翻译过程中，翻好一段，确认之后就可以删除原始英文内容了。保留不译的部分除外，不要保留原始内容在 .cnx 档中。
  1. changelog 可以不译。
  1. 尽量保持 Vim doc 格式，一般来说，格式跟原始档一致就可以了，建议在 Vim 中翻译，可以预览格式。

## 3. 标记(tags) ##
在 tags 目录下，保留了各个 Plugin 的多个版本翻译记录。比如 vimwiki 就包含
v0.9.9 和 v1.0 两个版本。vimwiki\_v0.9.9 和 vimwiki\_v1.0 目录下都存有各自版本
对应的英文原始档(.txt)。

所以大家可以把原始档放到 tags 目录里。等中文文档翻译并检查完成后，可以打 tags
到对应的目录。

Windows 下如果安装了 TortoiseSVN，右键目标文件（如 plugin.cnx），TortoiseSVN ->
Branch/tag...，浏览 "to URL:" 到目标目录（如 tags/doc/vimwiki\_v1.0/vimwiki.cnx）

如果不会打标签(tags)，可以联系 闲耘(hotoo.cn(AT)gmail.com) 来完成打标签。
**注意** 打标签是有意义的，相当于版本里程碑(例如 v1.0, v2.0)，请不要随意操作，谢谢。

## 4. Wiki ##
wiki 目录存放是项目 Wiki，即 http://code.google.com/p/vim-script-cn/w/list
里面的内容。

完成翻译请同步更新 PLAN.wiki 里的进度。
有好的 Plugin 也请增加到里面。

## 5. 范例 (翻译新文档: plugin.txt v1.0) ##
  1. 从 https://vim-script-cn.googlecode.com/svn/ checkout 项目。
  1. 复制要翻译的原始文档(plugin.txt 或 plugin.jax) 到 trunk/doc 目录，并重命名为 plugin.cnx
> > 另复制一份原始档到 tags/doc/plugin\_v1.0/plugin.txt
  1. 在 plugin.cnx 中进行翻译，完成一段就删除原文（注意先检查一下翻译结果）。
  1. 文档不懂的地方可以保留不译，或者请教他人。
  1. 可以随时提交，但建议完成较多的内容之后再统一提交。
  1. 全部完成后，提交到主干(trunk)。
  1. 打标签(tags)到 tags/doc/plugin\_v1.0/plugin.cnx

## 6. 范例 (翻译文档新版本: 从 v1.0 到 v2.0) ##
  1. 复制 plugin.txt v2.0 版到 tags/doc/plugin\_v2.0/plugin.txt
  1. 比较 plugin.txt 原始档 v2.0 和 v1.0 版的变化。
  1. 补充/删除/修正不同的部分即可。
  1. 完成后提交到主干(trunk)。
  1. 打标签到 tags/doc/plugin\_v2.0/plugin.cnx

## 7. 分工 ##
对于由多人分工合作翻译的文档，参与者最好事先商定各自负责的内容。

合并时，除自己负责的内容外，均以他人的为准。