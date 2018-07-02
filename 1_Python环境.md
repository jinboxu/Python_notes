##Python环境

###python虚拟环境的使用

参考文档：

> https://blog.csdn.net/shaququ/article/details/54292043
>
> https://www.cnblogs.com/cq146637/p/9033010.html



####Window 下创建python的虚拟环境

**下载工具**

　　pip install virtualenv

**创建虚拟环境目录**

　　# 注意此命令创建的虚拟环境目录是在当前目录下

　　virtualenv testenv

**使用虚拟环境**

　　cd testenv/Scripts

　　activate

**退出虚拟环境**

　　deactivate.bat

**指定使用python版本创建虚拟环境**

　　virtualenv -p C:\Python\Python36\python.exe testenvenv3



####Linux 下创建python的虚拟环境

**下载工具**

　　sudo apt-get install python-virtualenv

　　sudo yum install python-virtualenv

**创建虚拟环境目录**

　　virtualenv testenv2

**使用虚拟环境**

　　cd testenv2/bin

　　source activate

**退出虚拟环境**

　　deactivate

**指定使用python版本创建虚拟环境**

　　virtualenv -p /usr/bin/python3 testenv3

**由于每次使用虚拟环境都要记住路径，使用极为不方便**

virtualenvwrapper虚拟环境管理包，推荐使用

 

####Windows下使用virtualenvwrapper

**安装**

　　pip install virtualenvwrapper-win

**创建虚拟环境**

　　mkvirtualenv <venv_dir_name>

**指定使用python版本创建虚拟环境**

　　mkvirtualenv --python=C:\Python\Python36\python.exe testenv3

**创建的虚拟环境统一存放在**

　　C:\Users\<Username>\Evns

**修改默认存放路径**

　　添加一个环境变量，系统设置中添加

　　WORKON_HOME E:\Python Project\Evns

**查看所有的虚拟环境**

　　workon

**进入虚拟环境**

　　workon <venv_dir_name>

**退出虚拟环境**

　　deactivate.bat

 

####Linux下使用virtualenvwrapper

**安装**

　　pip install virtualenvwrapper

**寻找文件安装路径**

　　sudo find / -name virtualenvwrapper.sh

**存放路径**

　　/home/<username>/.local/bin/virtualenvwrapper.sh

　　/usr/local/bin/virtualenvwrapper.sh

**修改默认存放路径配置脚本生效**

　　vim ~/.bashrc

　　　　export WORKON_HOME=$HOME/.virtualenvs

　　　　source /home/<username>/.local/bin/virtualenvwrapper.sh

　　source ~/.bashrc

**创建虚拟环境**

　　mkvirtualenv <venv_dir_name>

**指定使用python版本创建虚拟环境**

　　mkvirtualenv --python=/usr/bin/python3 testenv3