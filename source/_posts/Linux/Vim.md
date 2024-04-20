# vimrc
1. 设置显示行号
   ```bash
vim~/.vimrc
set nu  
set nonu
```

2. 取消高亮
```bash
:noh
```
http://c.biancheng.net/view/809.html

3. 文本替换
4. https://www.myfreax.com/vim-find-replace/
```bash
:s/foo/bar/ #仅替换光标所在行的第一个匹配项
:s/foo/bar/g #替换光标所在行的所有匹配项

:%s/foo/bar/g #在整个文件中搜索替换foo
:s/foo//g #将光标当前行的foo替换为空字符串

```

# 撤销
u是撤销你刚才做的动作
ctrl+r 是恢复你刚才撤销的动作
