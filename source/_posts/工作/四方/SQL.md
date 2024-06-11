#  kingbaseV7
1. 更改了表名后，需要执行一下SQL语句，并且需要重新配置所有字段
```SQL
-- 刷新1号表，2号表，并配置
select init_sys_table('nccs_seqctrl_ticketname');
select init_sys_column('nccs_seqctrl_ticketname');
```
