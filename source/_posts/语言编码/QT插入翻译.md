您可以使用lupdate命令来更新.ts文件，该命令会扫描源代码中的所有字符串，并将新的或修改过的字符串添加到.ts文件中，同时保留已经翻译的条目。例如：
lupdate your_project.pro -ts your_translation.ts
这样，您就可以在不丢失已有翻译的情况下，将新的字符串添加到翻译文件中。

参数-qm指定生成qm文件的位置
lrelease  .ts -qm .qm