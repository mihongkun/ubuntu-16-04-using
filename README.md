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

#### 5.安装常用常用软件
* 安装搜狗拼音输入法，下载安装，配置，重启，选在搜狗输入法为第一个 地址(可能会有变化):http://pinyin.sogou.com/linux/download.php?f=linux&bit=64
* atom的安装: https://atom.io/download/deb
* sublime text安装：https://download.sublimetext.com/sublime_text_3_build_3126_x64.tar.bz2
* vsc 安装: https://code.visualstudio.com/docs/?dv=linux64_deb


#### 6.下载并安装jdk
* http://www.oracle.com/technetwork/java/javase/downloads/jdk8-downloads-2133151.html
* $sudo su 
* #mkdir /usr/lib/jvm
* #tar -C /usr/lib/jvm -zxf file_name ,这里的file_name指代是压缩文件tar -v会输出解压过程所以略过不用
* #vim /etc/profile 在最后添加:
    # SET ORACLE JDK ENVIRONMENT
    export JAVA_HOME=/usr/lib/jvm/jdk1.8.0_131
    export JRE_HOME=${JAVA_HOME}/jre
    export CLASSPATH=.:${JAVA_HOME}/lib:${JRE_HOME}/bin
    export PATH=${JAVA_HOME}/bin:$PATH 

