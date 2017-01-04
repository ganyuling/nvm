nvm、npm、bower安装和配置详细教程

先安装nvm,接着nodejs,最后安装npm、bower
nvm下载地址https://github.com/coreybutler/nvm-windows/

nvm详细安装步骤：
一：以管理员身份运行install.cmd文件，设置文件路径

root: C:\dev\nvm

path: C:\dev\nodejs

arch: 64

proxy: none

确保目录下有一个setting.txt文件（图片是我配置好后的截图，默认没有那些文件夹）

cmd 命令行输入nvm回车看到nvm的版本号表示nvm安装成功

 下载需要的nodejs版本https://nodejs.org/en/download/releases/
 ，解压后改名（如v6.9.1）放到nvm目录，注意里面如果有嵌套文件夹就把文件拿到外层

二：环境变量配置：点击我的电脑》属性》高级设置》环境变量》

1.删除系统自带的nvm变量：NVM_HOME和NVM_SYMLINK

2.打开path：删除nvm自动添加的变量C:\dev\nvm;C:\dev\nodejs

3.配置用户变量：

NVM_HOME = C:\dev\nvm

NVM_SYMLINK = C:\dev\nodejs

Path = %NVM_HOME%;%NVM_SYMLINK%

配置完成保存

4.cmd命令行：nvm use 6.9.1（安装需要的版本），32位系统（nvm use 6.9.1 32），看到Now useing node v6.9.1表示安装成功
同时会在nvm同级目录下有个nodejs快捷文件夹，想要那个版本就切换到那个版本，例如（nvm use 7.2.0）
