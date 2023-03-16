提取字符串中的数字
```bash
echo hgdfjg678gfdg kjg45nn | tr -d -c 0-9 # 输出 67845
```

```bash
temp = `echo "helloworld20181212 | tr -cd "[0-9]""` 
echo ${temp}
# helloworld
```

 