## 单节点hadoop的环境配置

* 准备工作

```
1. java环境已配好（ hadoop是依赖于java）
   用lxx用户登录配置环境
   java环境的操作步骤如下
```
[java环境](https://lixiaoxiaolove.github.io/Lixiaoxiao/boke/shell/case3)

* 配置工作

```
2. jar.gz下载解压
	把解压或的文件放在用户的根目录下,
	进入到hadoop的bin目录下，可以执行hadoop命令，
	但不在该目录下就不能执行
	
3. hadoop的环境变量PATH ---> hadoop的命令在哪能使用 bin: sbin
   在根目录下的.bash_profile里或/etc/profile里配置java环境
   export HADOOP_HOME=/home/yyc/hadoop-2.7.3
   PATH=$PATH:$HOME/bin:$HADOOP_HOME/bin:$HADOOP_HOME/sbin
   若测试hadoop命令成功，则环境配置完成
```

* 测试工作

```   
4. hadoop使用mapreduce计算了我们hadoop的配置文件的匹配内容

   hadoop的命令，从input文件里读取，结果输出到output中，正则表达式
   hadoop jar ~/hadoop-2.7.3/share/hadoop/mapreduce/hadoop-mapreduce-examples-2.7.3.jar 
		grep input/ output/ 'dfs[a-z]+'
   
   hadoop jar /home/yyc/hadoop-2.7.3/share/hadoop/mapreduce/hadoop-mapreduce-examples-2.7.3.jar 
		wordcount /home/yyc/lxxdate/test.txt /home/yyc/lxxput

```