参考教程：

https://blog.csdn.net/future_ai/article/details/81701744  

https://jingyan.baidu.com/article/aa6a2c14e11f030d4d19c457.html  

ubuntu可能无法直接连通ssh。需要先  
apt-get install openssh-server  
apt-get install openssh-client  

然后  
sudo vi /etc/ssh/ssh_config  
去掉PasswordAuthentication yes前面的#号，保存退出  

然后  
sshd_config中把PermitRootLogin prohibit-password改成PermitRootLogin yes，保存退出。    
重启ssh服务    
sudo /etc/init.d/ssh restart    
 
ifconfig查看ip，inet后就是ip。然后不用接网线，直接使用相同wifi的win10即可连接。  

