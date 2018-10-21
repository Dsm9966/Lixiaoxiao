### 文件操作命令
	* touch
		* 用途：新建空文件，或更新文件时间标记
		* touch	文件路径
	* > 
		* > 文件路径
	* echo 
		* echo "要加入的内容" >> 文件路径
		* 若该文件存在，在末尾处开始添加，若不存在，就新建
	* file
		* 用途：查看文件类型
		* file 文件路径
		![](https://upload-images.jianshu.io/upload_images/14466013-50fb35d8db8ce4d0.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
	* cp
		* 用途：复制（copy）文件或目录
		* cp [选项] 源文件或目录…   目标文件或目录
		* 常用命令选项
			* -r：递归复制整个目录树
			![](https://upload-images.jianshu.io/upload_images/14466013-deb715b0092258a9.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
			* -p：保持源文件的属性不变
			* -f：强制覆盖目标同名文件或目录？？？？？？？？？？？？？
			* -i：需要覆盖文件或目录时进行提醒
	* rm
		* 用途：删除文件或目录
		* rm [选项] 文件或目录
		![](https://upload-images.jianshu.io/upload_images/14466013-a799ccd2903f9dc7.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
		* 常用命令选项
			* -f：强行删除文件，不进行提醒
			![](https://upload-images.jianshu.io/upload_images/14466013-751ec28052fe8cdd.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
			* -i：删除文件时提醒用户确认
			* -r：递归删除整个目录树
			![](https://upload-images.jianshu.io/upload_images/14466013-2fa8c723b871e3eb.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
	        ![](https://upload-images.jianshu.io/upload_images/14466013-ca3ba21f1c8b8a15.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
	* mv
		* 用途：移动（Move）文件或目录—— 如果目标位置与源位置相同，则相当于改名
		* mv [选项]... 源文件或目录 目标文件或目录
	* which
		* 显示系统命令所在目录
		* which	<选项>	command（命令名称）
		![](https://upload-images.jianshu.io/upload_images/14466013-486e0a6d4ba427a9.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
		* 常用命令选项
			* -a：将所有由PATH路径中可以找到的指令均列出，而不止第一个被找到的指令名称
	* find
		* find <路径> <选项> [表达式]
		* find查找的特点
			* 从指定路径下递归向下搜索文件、
			* 支持按照各种条件方式查找
			* 支持对查找到的文件再进一步的使用指令操作
			* （例如：删除、统计大小、复制等）
		*  常用命令选项
			* -name	 根据文件名查找
			* -user	 根据文件拥有者查找
			* -group 根据文件所属组寻找文件
			* -perm	 根据文件权限查找文件
			* -size	 根据文件大小查找文件
			* -type	 根据文件类型查找（f-普通文件，c-字符设备文件，b-块设备文件，l-链接文件，d-目录）
			* -o	 表达式或
			* -and	 表达式与
	* 快捷键
			* ctrl + c（停止当前进程）
			* ctrl + r（查看命令历史）
			* ctrl + l（清屏，与clear命令作用相同）