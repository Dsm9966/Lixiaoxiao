* �鿴�û��������Ϣ
	* vim /etc/passwd
	![yonghu.png](https://upload*images.jianshu.io/upload_images/14466013*e6377a37fa82b2c7.png?imageMogr2/auto*orient/strip%7CimageView2/2/w/1240)
	![jianjie.png](https://upload*images.jianshu.io/upload_images/14466013*e6377a37fa82b2c7.png?imageMogr2/auto*orient/strip%7CimageView2/2/w/1240)
* �鿴�û�����������Ϣ
	* ע��Ȩ�����⣬����Ȩ�ޣ�ʹ��su�����л���root�û��ڲ���
	![image.png](https://upload*images.jianshu.io/upload_images/14466013*78f5f8a7f794351d.png?imageMogr2/auto*orient/strip%7CimageView2/2/w/1240)
	* vim /etc/shadow
	![image.png](https://upload*images.jianshu.io/upload_images/14466013*f2b5ac1762b2aed9.png?imageMogr2/auto*orient/strip%7CimageView2/2/w/1240)
	![image.png](https://upload*images.jianshu.io/upload_images/14466013*db4601ef4da70cb7.png?imageMogr2/auto*orient/strip%7CimageView2/2/w/1240)
* ����û� 
	* ���� useradd [] �û���
	* ѡ��
		* -u ָ����ID��uid��
			* eg
			![image.png](https://upload*images.jianshu.io/upload_images/14466013*bb23e7ebce7fc321.png?imageMogr2/auto*orient/strip%7CimageView2/2/w/1240)
			* ���н��
			![image.png](https://upload*images.jianshu.io/upload_images/14466013*f0ec08aceea36e19.png?imageMogr2/auto*orient/strip%7CimageView2/2/w/1240)
			* uid���ֶ���ӣ�ϵͳ���Զ����
			![image.png](https://upload*images.jianshu.io/upload_images/14466013*5def2cb554d96686.png?imageMogr2/auto*orient/strip%7CimageView2/2/w/1240)
		* -g ָ��������������gid��
			* ָ����gidһ�����Ѿ����ڵ���id���������ڣ������
			![image.png](https://upload*images.jianshu.io/upload_images/14466013*d5f56674c64da312.png?imageMogr2/auto*orient/strip%7CimageView2/2/w/1240)
			* ���н��
			![image.png](https://upload*images.jianshu.io/upload_images/14466013*3e8305f19b7c8e60.png?imageMogr2/auto*orient/strip%7CimageView2/2/w/1240)
		* -G ָ������飬�ö��š������ֿ���Groups��
		* -c �û�������comment��
		* -e ʧЧʱ�䣨expire date��
* �޸��û�����
	* ���� usermod [] �޸ĺ���û��� ���޸ĵ��û���
	* ѡ��
		* -l �޸��û��� 
			* usermod *l a b            b��Ϊa
			* ���
			![image.png](https://upload*images.jianshu.io/upload_images/14466013*130cabc5f4709f8c.png?imageMogr2/auto*orient/strip%7CimageView2/2/w/1240)
			![image.png](https://upload*images.jianshu.io/upload_images/14466013*d45401ce0e2d26ff.png?imageMogr2/auto*orient/strip%7CimageView2/2/w/1240)
		* -g ����� 
			* usermod *g sys tom        tom�û���ӵ�sys��
			* ���
			![image.png](https://upload*images.jianshu.io/upload_images/14466013*2c9595eaceec534c.png?imageMogr2/auto*orient/strip%7CimageView2/2/w/1240)
			![image.png](https://upload*images.jianshu.io/upload_images/14466013*e70d5cb5a17927fe.png?imageMogr2/auto*orient/strip%7CimageView2/2/w/1240)
		* -G ��Ӷ���� 
			* usermod *G sys,root tom   tom�û���ӵ�sys��root����
			* �����Ҫ�� /etc/group�в鿴���
			![image.png](https://upload*images.jianshu.io/upload_images/14466013*a072b9db374aea46.png?imageMogr2/auto*orient/strip%7CimageView2/2/w/1240)
		    ![image.png](https://upload*images.jianshu.io/upload_images/14466013*842046408c702a96.png?imageMogr2/auto*orient/strip%7CimageView2/2/w/1240)
		* �CL �����û��˺�����
		* �CU �����û��˺�
* ɾ���û�����
	* ���� userdel [] �ļ�����·��
	* ѡ��
		* -r ɾ���˺�ʱͬʱɾ��Ŀ¼
		* ���
		![image.png](https://upload*images.jianshu.io/upload_images/14466013*422b91cbce4f6d80.png?imageMogr2/auto*orient/strip%7CimageView2/2/w/1240)
		* ע��
		![image.png](https://upload*images.jianshu.io/upload_images/14466013*22264a8e55c30dae.png?imageMogr2/auto*orient/strip%7CimageView2/2/w/1240)