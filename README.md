中文导入下载中文包，部分已经无法下载了，下面是一个可用的。

ubuntu 导入中文
在Ubuntu中导入中文字符集通常涉及到配置系统的语言设置以及安装中文字体。以下是简要步骤和示例代码：

安装中文语言支持包：

sudo apt-get update
sudo apt-get install language-pack-zh-hans
配置系统语言：

打开终端。

查看当前语言设置：

locale

如果需要，编辑/etc/default/locale文件，添加或修改以下行：

LANG="zh_CN.UTF-8"
LANGUAGE="zh_CN:zh"

应用更改：

sudo locale-gen zh_CN.UTF-8
sudo update-locale LANG=zh_CN.UTF-8

安装中文字体（如果需要）：

sudo apt-get install fonts-wqy-zenhei
重新启动你的会话或者系统，以确保所有的设置生效。

变量	含义
LC_CTYPE：	语言符号及其分类
LC_NUMERIC：	数字
LC_TIME：	时间显示格式
LC_COLLATE：	比较和排序习惯
LC_MONETARY：	货币单位
LC_MESSAGES：	信息，如提示信息、错误信息、状态信息、标题、标签、按钮和菜单等
LC_PAPER：	默认纸张大小
LC_NAME：	姓名书写方式
LC_ADDRESS：	地址书写方式
LC_TELEPHONE：	电话号码书写方式
LC_MEASUREMENT：	度量衡表达方式
LC_IDENTIFICATION：	locale 对自身包含信息的概述
————————————————



1.修改 /etc/profile 文件
在 /etc/profile 文件代码的最后添加定义环境变量的语句，然后执行 sudo source /etc/profile 后注销生效。如：

sudo vim /etc/profile
export LANG=zh_CN.UTF-8
export LANGUAGE=zh_CN:zh
1
2
3
这种方法比较可靠，因为这个环境变量的调用发生在系统启用的最后阶段。
————————————————

                            版权声明：本文为博主原创文章，遵循 CC 4.0 BY-SA 版权协议，转载请附上原文出处链接和本声明。
                        
原文链接：https://blog.csdn.net/ymz641/article/details/131607024

q1:出现乱码，而且有一部分文字能够输入，实际上是因为输入的vimrc有部分设定导致的。
