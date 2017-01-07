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

使用：

查看已安装的版本： nvm ls

查看可以安装的版本：nvm ls-remote

安装指定的版本： nvm install <version>

删除指定的版本： nvm uninstall <version>

使用选定的版本： nvm use <version>


npm和cnpm使用

1、使用npm安装插件：命令提示符执行npm install <name> [-g] [--save-dev] 

2、使用npm卸载插件：npm uninstall <name> [-g] [--save-dev]   PS：不要直接删除本地插件包 

3、使用npm更新插件：npm update <name> [-g] [--save-dev] 

4、更新全部插件：npm update [--save-dev] 

5、查看npm帮助：npm help 

6、查看当前目录已安装插件：npm list

PS：npm安装插件过程：从http://registry.npmjs.org下载对应的插件包（该网站服务器位于国外，所以经常下载缓慢或出现异常），解决办法往下看↓↓↓↓↓↓。

选装cnpm

安装：命令提示符执行npm install cnpm -g --registry=https://registry.npm.taobao.org
使用和npm一样

使用gulp推荐http://www.ydcss.com/archives/18
