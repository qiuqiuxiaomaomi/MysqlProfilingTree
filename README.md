# MysqlProfilingTree
Mysql慢查询，性能瓶颈问题研究


<pre>
     当我们要对某一条sql的性能进行分析时，可以使用它。

     Profiling是从 mysql5.0.3版本以后才开放的。
     启动profile之后，所有查询包括错误的语句都会记录在内。
     关闭会话或者set profiling=0 就关闭了。（如果将profiling_history_size参数设置为0，
     同样具有关闭MySQL的profiling效果。）

     此工具可用来查询SQL执行状态，System lock和Table lock 花多少时间等等，

     对定位一条语句的I/O消耗和CPU消耗 非常重要。(SQL 语句执行所消耗的最大两部分资源就是IO和CPU)
</pre>

<pre>
查询profile是否打开
SELECT @@profiling;

       1）输出0说明profiles功能是关闭的
         开启profiles功能
         > set profiling=1;

       2）show profiles;

       3）show profile all for query 66;
</pre>

![](https://i.imgur.com/GF7GRoI.png)
