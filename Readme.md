创建密钥分两大步，但首先必须y要有github账户。

#：安装配置git服务器

## 安装ssh，因为git是基于ssh协议的，所以必须先装ssh：

###
```
sudo apt-get install openssh-server openssh-client

```
### 安装好ssh后，启动ssh服务：

```
sudo /etc/init.d/ssh restart

```
##  安装git服务器：

```
sudo apt-get install git-core

```

# 配置ssh公钥

##    首先在本地生成ssh公钥

```
ssh-keygen -C 'your emaildress' -t rsa

```
如：ssh-keygen -C 'yueyueni_zhao@163.com' -t rsa
会在用户目录～/.ssh/下建立相应的密钥文件

*此处应该注意的是不要修改在.ssh 中要生成文件的名字！

可以使用ssh -v git@github.com命令来测试链接是否畅通

```
ssh -v git@github.com

```
##上传公钥至github

  在账户的profile里，选择SSH KEYS 选项，然后Add SSH Key，将~/.ssh/id_rsa.pub中的内容复制进去，上传。
  上上传成功后，会收到确认邮件。 可以使用ssh -v git@github.com命令来测试链接是否畅通。

在最后的是在你的仓库中的 clone and download 下选择 use SSH,然后进行上传。

一般本地文件先要
```
git init

```''''
