## hiveʹ��

1 cli��shell�ն������У�
1.1 ��ʹ��hive�������hive����
1.2 �ڽ���select�Ȳ���
2. jdbc����hive�Ļ���jdbc�����ṩ�Ŀͻ��ˣ�
   �û�ͨ��jdbc������hive server��ͨ�����������hive
2.1 ����shell����hive������mysql������namenode��datanode
    ���� hiveserver2 �ű�
2.2 �ڿ�һ����ip�ĻỰ������ beeline ������û���
2.3 �� !connect jdbc:hive2://localhost:10000 �������ӣ�
    ��ָ�������û��������루��û�����ûس���
2.4 ����select�Ȳ���

## hive��ΪʲôҪ��Ԫ���ݿ⣨mysql����

��Ϊhive������Ӧ�������Ǵ洢��hdfs�ϵģ����������������Ǵ���datanode�ϵģ�
��Ҫ�ҵ�datanode�ϵ����ݣ����Ǿ���Ҫ������������м�¼

## �ڲ������ⲿ�������

1.1 �����ڲ���
    create table innerlxx(id int,name string) 
    row format delimited fields terminated by '\t';
1.2 �����ⲿ��
    create external table exlxx(id int,name string) 
    row format delimited fields terminated by '\t' 
    location '/dbdata/';
1.3 ͨ���ؼ��� external ����������
1.4 ��Ϊ�ⲿ�����������������ⲿ�����ݣ����Ҳ�ϣ����ԭʼ���ݽ����ƻ���
    ����Ҫ���location ��ָ���ⲿ��Ҫ��ȡ���ݵ�ɫλ��
1.5 ��ɾ�����������ʱ���ڲ����ǰ����е����ݶ�����ɾ��
    ���ⲿ����ǰѱ�Ĺ�����Ϣ����ɾ����Ԫ���ݲ��ض�ʧ
1.6 load data inpath '/dbdata/women.log' into table exlxx;
   ��hdfs�Ͻ������ݵ�����ǽ�hdfs�ϵ������ƶ���table��ʹ�õ�Ŀ¼�£�����Ԫ������ʧ��

## ������

�൱���ڱ����ַ���С��
�����ǿ��Լ���������һ������ʱ�Ĳ�ѯ�����������������ǵĲ�ѯЧ��
��������ֻ��һ�㣬���ǿ��Դ�����������ʽ����С��������С��
1.1 create table lxxpart(id int,name string)
    partitioned by(year string,month string) 
    row format delimited fields terminated by '\t';
1.2 �����÷�����Ҫ�������ݵĵ��룬Ҫ������Ҫָ���ý����ݵ��뵽�ĸ�������
    ����ϵͳ��֪�������ݷ����ĸ����������磺
    load data inpath '/dbdata/user.log' into table lxxtime partition(yaer='2017',month='01');
1.3 ������̫�࣬�����ö�̬����
1.4 �鿴���������Ϣ
    show partitions lxxpart;
    show partitions ����;

## ��̬����

1. ʹ�ó���
   ��������Ҫ�����ݽ��з�����ʱ�������õ������ݲ�һ�����Ѿ��ֺ������ļ���
   ���ԾͲ���ֱ��load������ʹ�ã���ʱ���Ҫ�ö�̬����������������������ļ���
user.log
1	tangceng	02	man
2	wukong		03	man
3	xioabailong	06	man
4	nvshen		08	woman
5	xioameinv	11	woman

2. ���������ļ������㰴�·ݽ��з���
2.1 �����ҵ����ݴ���һ������
    load data inpath '/dbdata/user.log' into table users;
2.2 ������Ӧ�ķ�����
    create table birthdays(id int,name string,month string,sex string)
    partitioned by(month string) 
    row format delimited fields terminated by '\t';
2.3 �������̬�����ĳ�������
    insert into birthdays partition(month)
    select id,name,month from users;
2.4 ��Ҫ���ж�̬�����Ͳ�Ҫ�� partition(month) �и��������ù̶�ֵ
2.5 Ĭ��ʹ�õ����ϸ�ģʽ���ǲ�����̬�����ģ�����������Ҫ��������ִ��
    set hive.exec.dynamic.partition.mode=nonstrict
2.6 ʹ�ö�̬�����Ὣ����������һ����Ϊ�������������Բ�ѯʱҪע��