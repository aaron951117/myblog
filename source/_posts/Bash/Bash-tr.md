---
title: Bash-tr
top: false
cover: false
toc: true
mathjax: false
date: 2023-03-15 17:36:42
author:
img:
coverImg:
password:
summary:
tags:
categories:
---

tr [选项]... SET1 [SET2]

选项包括下面的:
-   -c, -C, --complement 首先补足SET1
-   -d, --delete 删除匹配SET1 的内容，并不作替换
-   -s, --squeeze-repeats 如果匹配于SET1 的字符在输入序列中存在连续的重复，在替换时会被统一缩为一个字符的长度

SET1包括：

\NNN 八进制值为NNN 的字符(1 至3 个数位)
\ 反斜杠
\a 终端鸣响
\b 退格
\f 换页
\n 换行
\r 回车
\t 水平制表符
\v 垂直制表符
字符1-字符2 从字符1 到字符2 的升序递增过程中经历的所有字符
[字符*] 在SET2 中适用，指定字符会被连续复制直到吻合设置1 的长度
[字符*次数] 对字符执行指定次数的复制，若次数以 0 开头则被视为八进制数
[:alnum:] 所有的字母和数字
[:alpha:] 所有的字母
[:blank:] 所有呈水平排列的空白字符
[:cntrl:] 所有的控制字符
[:digit:] 所有的数字
[:graph:] 所有的可打印字符，不包括空格
[:lower:] 所有的小写字母
[:print:] 所有的可打印字符，包括空格
[:punct:] 所有的标点字符
[:space:] 所有呈水平或垂直排列的空白字符
[:upper:] 所有的大写字母
[:xdigit:] 所有的十六进制数
[=字符=] 所有和指定字符相等的字符






