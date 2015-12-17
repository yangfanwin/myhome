# myhome

##创建SSH密钥
    1.ssh-keygen -b 1024 -t rsa
	   -b 指密钥对长度  -t 指加密方式
      Enter file in which to save the key (/c/Users/yangfan/.ssh/id_dsa): 
       回车，默认位置即可
    2.输入密码
    3.上传SSH密钥
       打开Key保存的位置，里面会有三个文件，找到id_rsa.pub，用文本编辑器打开，
    复制里面的全部字符，到GitHub，在右上方工具栏里找到Settings，在这个页面上有一个
    SSH Public Keys标签，选择Add another public key，Title可以随便填一个，Key就
    粘贴刚才的字符，提交。

##同步工程到github
    1.右键启动Git Bash命令行
    2.配置github账号
   		git config --global user.name "yangfanwin"
   		git config --global user.email "yangfanwin@163.com"
 	3.新建工程
   		git clone https://github.com/yangfanwin/myhome.git
 	4.拷贝工程内容到myhome目录
 	5.提交工程
   		git add .   
   		git commit -m "changes log" 
   		git remote add origin git@github.com:yangfanwin/myhome.git
   		git push -u origin master

##提交代码
    git add .   
   	git commit -m "changes log"
   	git push -u origin master

##异常解决
    1.warning: LF will be replaced by CRLF
   		rm -rf .git  
   		git config --gobal core.autocrlf false