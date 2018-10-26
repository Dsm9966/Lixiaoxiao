## ������
* java����������
```
#��һ���µĻ����У���û��java���������ã���Ŀ¼�е�/home/yyc/bin��
#�½�һ��shell�ű�
> javaPath.sh
#����༭
vim javaPath.sh


#!/bin/bash
#���������ذ�װ��
wget  --no-check-certificate --no-cookies --header "Cookie: oraclelicense=accept-securebackup-cookie" 
http://download.oracle.com/otn-pub/java/jdk/8u191-b12/2787e4a523244c269598db4e85c51e0c/jdk-8u191-linux-x64.tar.gz
#�ӵ�ǰĿ¼���Ұ�װ��
javatar=$(ls | sed -n '/jdk.*gz$/p')
#��ѹ��װ��
tar -zxf $javatar
#ɾ��ѹ���İ�װ��
rm -rf $javatar
#��ȡjdk��·��
jdkname=$(ls | grep jdk)
#�����·��
cd $jdkname
#�õ����ڵ�·��
javaname=$(pwd)
#�� /etc/profie����ӻ�������
echo "export JAVA_HOME=$javaname" >> /etc/profile
echo 'export PATH=$PATH:$JAVA_HOME/bin' >> /etc/profile
echo 'export CLASSPATH=$:CLASSPATH:$JAVA_HOME/lib/' >> /etc/profile
#���и������ļ�
. /etc/profile

```