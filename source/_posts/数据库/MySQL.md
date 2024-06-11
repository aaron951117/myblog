---
title: MySQL
top: false
cover: false
toc: true
mathjax: false
date: 2023-05-05 14:31:31
author: TianShan
img:
coverImg:
password:
summary:
tags:
categories:
---
# MySQL-8.0
```mysql
# MySQL5.7以后，password字段不再存在，变成了authentication_string
SELECT User, Host, authentication_string FROM mysql.user;
# 给某个用户修改密码
ALTER USER 'pig'@'%' IDENTIFIED WITH mysql_native_password BY '1234';
```



```sql
# 当修改表设置联合主键时删除不符合的记录保留最大id记录
# 查询记录
SELECT bay_id, source_states, target_states, seq_ctrl_type
FROM nccs_onekeyctrl_operticket
GROUP BY bay_id, source_states, target_states, seq_ctrl_type
HAVING COUNT(*) > 1;


# 当修改表设置联合主键时删除不符合的记录保留最大id记录
DELETE FROM nccs_onekeyctrl_operticket
WHERE id IN (
    SELECT id
    FROM (
        SELECT id
             , MAX(id) OVER (PARTITION BY bay_id, source_states, target_states, seq_ctrl_type) AS max_id
        FROM nccs_onekeyctrl_operticket
        WHERE (bay_id, source_states, target_states, seq_ctrl_type) IN (
            SELECT bay_id, source_states, target_states, seq_ctrl_type
            FROM nccs_onekeyctrl_operticket
            GROUP BY bay_id, source_states, target_states, seq_ctrl_type
            HAVING COUNT(*) > 1
        )
    ) AS max_id_records
    WHERE id <> max_id
);
```
