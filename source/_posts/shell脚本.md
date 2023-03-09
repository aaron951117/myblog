1. 查看字典里某个键名是否存在
```shell
if [ -v dic["key1"] ]; then echo "key1 exists in dic" fi
```
2. 遍历字典
```shell
for key in "${!dic[*]}"
do
	echo "$key - ${dic[*]}"
done

# 逐对遍历
for key in $(echo ${!dic[*]})
do
	echo "$key - ${dic[$key]}"
done
```
3. 一次性获取字典的键值对和键值
```shell
values=${dic[*]} // 获取字典中所有的值的列表
keys=${!dic[*]} // 获取字典中所有的键的列表
```
4. 遍历列表值
```bash
for i in ${a[*]}; 
do  
	echo ”$i“
done
```


## 取特定类型
1. 字符串中取数字
```bash
temp = `echo "helloworld20181212 | tr -cd "[0-9]""` 
echo ${temp}
# helloworld
```
2. 数组
```bash
### Shell 数组元素个数
${#array[@]}
###数组的所有元素
${array[*]}
###字符串长度
${#str}
```
