## ����һ
* дһ��shell�ű��ܹ������е�ѹ�������н�ѹ
* toncat jdk hadoopѹ�������� /home/yyc/tar �£�yyc��һ���û���
	1. ��ȡ�û�Ҫ��ѹ��·������·���ò�������������"$1" ������ȡ��
	2. �Ӷ�ӦĿ¼��ȡ����Ҫ���н�ѹ���ļ�
	3. ����Щ�ļ�һ�����Ľ��н�ѹ
	
* eg��
```
#�� /home/yyc/bin���½�һ��shell�ļ�
touch lxxtar.sh
#�����ļ��ڽ��б༭
vim lxxtar.sh

#shells�ű��Ŀ�ͷ���ǹ̶���
#!/bin/bash

#��ѹ������·��������һ���ļ���
ls $1*.gz > /home/yyc/bin/tar.log
#ѭ�����ļ�
for file in $(cat /home/yyc/bin/tar.log)
#���н�ѹ����
do
	tar -zxf $file
	echo "$file�ѽ�ѹ���"
done


#���иýŲ�
. lxxtar.sh /home/yyc/tar/

```