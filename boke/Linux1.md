## Linux�����м���
    * �����ļ�
	  ![](https://upload-images.jianshu.io/upload_images/14466013-6f6e17b57b5ce608.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
	* �鿴���м���
		* ʹ��runlevel����ֱ���ʾ���л�ǰ�����м��𡢵�ǰ�����м���n ��ʾ֮ǰδ�л������м���
		  ![ͼ1.1](https://upload-images.jianshu.io/upload_images/14466013-63c92e5d0d84206e.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)![image.png](https://upload-images.jianshu.io/upload_images/14466013-63c92e5d0d84206e.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
	* ��ʱ�л����м�����ʱ�л����м���
	    *  ʹ��init������0-6���м������
		   ![ͼ1.2](https://upload-images.jianshu.io/upload_images/14466013-79eb308a1b11e70e.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
	* hostname����
        * �鿴��ǰ������
		  ![ͼ1.3](https://upload-images.jianshu.io/upload_images/14466013-e355bae5b59d54c9.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
		* ��ʱ�޸�(һ�����޸ģ���������ԭ����)
		  ![ͼ1.4](https://upload-images.jianshu.io/upload_images/14466013-bc28ff7bd903755f.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
		*  �����޸ģ��޸������ļ���
			*  /etc/hostname�ļ�
			*  ��;������ȫ���������ã���Ҫ������������Ϣ
			* ����
				* ʹ��vi������뵽�����ļ�
				* ��i ������б༭��֮���Ȱ�esc ���˳��༭״̬���ڰ�:wq���б����˳�
				* ��������ܿ���Ч��
				  ![ͼ1.4](https://upload-images.jianshu.io/upload_images/14466013-5c94c2d3c1a3e04b.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
		* ### ע��Ȩ�����⣬root��ӵ���޸���������Ȩ��
			* ���û��л���root�û�
			   ![ͼ1.5](https://upload-images.jianshu.io/upload_images/14466013-e121d710522d5026.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
			* �޸����ڴ�root�û��л�ԭ�û�
			   ![ͼ1.6](https://upload-images.jianshu.io/upload_images/14466013-44e5e44f5b0ccd2e.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
	* ping����
		* ����������ͨ��
		* ��ʽ��ping [ѡ��] Ŀ������
		* ctrl + c ��ֹ����
		  ![ͼ1.7](https://upload-images.jianshu.io/upload_images/14466013-4b6852e5ef4d6f4a.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
	* ifconfig
		* �鿴���л����ӿڵ���Ϣ
		   ![ͼ1.6](https://upload-images.jianshu.io/upload_images/14466013-d9125068b290b4a0.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
		* �鿴ָ������ӿ���Ϣ
			* ��ʽ��ifconfig IP
		* Ifconfig�����ã�ʹ��yum����
			* yum install net-tools -y
	* ���÷���ǽ
        * �鿴����ǽ״̬
			* service firewalld status
			![](https://upload-images.jianshu.io/upload_images/14466013-ed0a6797af818bf5.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
		* ��ʱ�رշ���ǽ
			* systemctl stop firewalld
			![](https://upload-images.jianshu.io/upload_images/14466013-346bddfcb16a8e85.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
 		* ���ùرշ���ǽ
			* �޸������ļ�
	* ��������ӳ���ļ�
		* ��;��������������IP��ַ��ӳ���¼
		* �鿴
		  ![](https://upload-images.jianshu.io/upload_images/14466013-819b4de6c879e530.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
	* ����������Ϣ
		* �鿴
		 ![](https://upload-images.jianshu.io/upload_images/14466013-2cde392efeb633ba.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
	* ����SELinux
		* ��������ȫ�ֿ����ģ���ȫ����ܸߣ����������ã���ʱ�����ض���ʱ�᲻������
		![](https://upload-images.jianshu.io/upload_images/14466013-70fa95938ac76186.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
		* �鿴SElinux�����ܷ��صĽ��������
			* Enforcing��ǿ��ģʽ�������¼��ȫ��������ֹ������Ϊ
			* Permissive������ģʽ�������¼��ȫ���浫����ֹ������Ϊ
			* Disable���ر�
		* ��ʱ�޸�
		  ![](https://upload-images.jianshu.io/upload_images/14466013-9cb3bced3356402e.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
		* �����޸�
		  ![](https://upload-images.jianshu.io/upload_images/14466013-840d2470a673ba95.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
