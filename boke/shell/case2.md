## ������
* ��������û�
```
#��/home/yyc/binĿ¼�´���һ��shell�ű�
> createUser.sh
#�����ļ����б༭
vim createUser.sh


#!/bin/bash

#�Ӽ�����������
read -p "������Ҫ�������û�����ǰ׺��" userName
#��forѭ��������û�
for (( i=0;i<=30;i=i+1 ))
do
	#�������û�
	useradd $userName$i
	#�����ʾ
	echo "�û�$userName$i�������"
	#���û��������
	echo "123456" | passwd $userName$i --stdin
done

```