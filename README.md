# ubuntu-16-04-using
---
**只为学习而写**

### learn using Ubuntu build a learning platform

#### 1.安装Ubuntu(此步骤对于我非常简单略过)
#### 2.更新系统
* 进入系统CTRL+ALT+t 打开一个命令窗口
* 输入命令 sudo su 输入密码 回车切换到超级用户
* 输入命令 apt update && apt upgrade -y 回车 更新系统

#### 3.设置hosts文件为安装chrome做准备
* 在shell中安装git -->$sudo apt install git -y
* 用git clone github上面的hosts -->$git clone https://github.com/racaljk/hosts.git
* clone完成之后，会在当前路径下(pwd命令可以查看当前路径)多出一个hosts目录，移动hosts文件到系统配置路径-->$mv hosts/hosts /etc/hosts

#### 4.安装chrome浏览器
* 打开系统自带的Mozilla Firefox浏览器，在地址栏中输入:https://google.com/ncr,并回车
* 在打开的google搜索栏里输入:chrome 64 bit dev ,并回车
* 或直接略过前两步直接在浏览器的地址栏中输入:https://www.chromium.org/getting-involved/dev-channel,并回车
* 之后做的事情就是下载系统对应版本的chrome浏览器
* 将浏览器下载到本地之后通过命令-->$sudo dpkg -i file_name，这里的file_name替换为chrome安装文件所在路径
* 一般会安装失败，这个时候再在命令行中执行下面命令即可安装成功:$sudo apt install -f -y
* 安装完成之后就可以在Application中查找到chrome浏览器的启动图标了