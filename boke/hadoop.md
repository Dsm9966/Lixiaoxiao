## ���ڵ�hadoop�Ļ�������

* ��yyc�û���¼���û���
* hadoop��������java
```
1. java������jdk��װ����
2. jar.gz���ؽ�ѹ
	�ѽ�ѹ����ļ������û��ĸ�Ŀ¼�£�
	���뵽hadoop��binĿ¼�£�����ִ��hadoop���
	�����ڸ�Ŀ¼�¾Ͳ���ִ��
3. hadoop�Ļ�������PATH---�� hadoop������������ʹ�� bin: sbin
   �ڸ�Ŀ¼�µ�.bash_profile�����ļ�������
	export HADOOP_HOME=/home/yyc/hadoop-2.7.3
	�޸�PATH��PATH=$PATH:$HOME/bin:$HADOOP_HOME/bin:$HADOOP_HOME/sbin
   ������hadoop����ɹ����򻷾��������
4. hadoopʹ��mapreduce����������hadoop�������ļ���ƥ������
#hadoop�������input�ļ����ȡ����������output�У�������ʽ
hadoop jar ~/hadoop-2.7.3/share/hadoop/mapreduce/hadoop-mapreduce-examples-2.7.3.jar 
	grep input/ output/ 'dfs[a-z]+'

```