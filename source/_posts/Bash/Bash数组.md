1. 遍历列表值
```bash
for i in ${a[*]}; 
do  
	echo ”$i“
done
```

2. 数组
```bash
### Shell 数组元素个数
${#array[@]}
###数组的所有元素
${array[*]}
###字符串长度
${#str}
### 数组结尾添加元素
array[${#array[@]}]=element
```
