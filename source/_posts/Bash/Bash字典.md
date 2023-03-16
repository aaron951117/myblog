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

