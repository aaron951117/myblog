1. python按照行进行读取
```python
with open('/path/to/file', 'r') as f:
	for line in f.readlines():
	    print(line.strip()) # 把末尾的'\n'删掉
```
