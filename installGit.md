#在github上发布东西

首先建立一个库 name

然后在线上加入README
在本地执行： 

1. git clone github.com/hzf-sbit/name
2. git init
3. git add .



#使用ssh同步上传

前提是有ssh..

1. git remote rm origin
2. git remote add orgin git@github.com:hzf-sbit/name.git
3. git push origin

#github添加本地ssh

1. ssh-keygen -t rsa -C "1436571029@qq.com"

returns:

Generating public/private rsa key pair.
# Enter file in which to save the key (/home/you/.ssh/id_rsa):

按enter继续

Enter passphrase (empty for no passphrase): [Type a passphrase]
# Enter same passphrase again: [Type passphrase again]

2. eval "$(ssh-agent -s)"

3. 安装xclip复制rsa

sudo apt-get install xclip
xclip -sel clip < ~/.ssh/id_rsa.pub

4. 把rsa添加到github
