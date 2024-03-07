# 碎碎念

​	SQLmap作为测试SQL注入的强有力工具深受广大用户的青睐，但由于非国人制作，绝大多数均为英文版，对于使用体验会有较大影响。同时仅仅只有命令行模式，需要记下大量命令和重复输入命令，因此本工具应运而生。 

# **工具介绍**

​	通过人工汉化，并针对中文与英文的语法区别，进行了特殊的代码修改，从而实现汉化后语句通顺，减小误会的产生。编写好的GUI文件直接进入图形化模式，通过鼠标勾选参数就可以快速执行命令，同时支持批量扫描。

# 快速上手

​	在文件夹中选择 gui.pyw 双击启动（请确认您的Python环境为Python3，运行py文件的方式为python sqlmap.py，如果并非该格式，请到gui.pyw中对应位置进行修改）
![aaee93427b4abf4c6ec2960724c80edd](https://github.com/honmashironeko/sqlmap-cn/assets/139044047/dd55065a-4cb8-40a4-838d-a55c90e96f7a)

请注意，如果您双击gui.pyw无法正常启动，请右键文件--属性--打开方式更改为python.exe，请注意不是pythonw.exe

![02f63769802ce75db8ec3b6a7c715ad3](https://github.com/honmashironeko/sqlmap-cn/assets/139044047/7c667cb5-cc6a-4d03-ad46-82da28c95759)

​	左侧选择命令，中间填入burp抓取的数据包，点击开始运行即可！
![e4ce8c7a9faade2d2fe151cae608b797](https://github.com/honmashironeko/sqlmap-cn/assets/139044047/05aa9b67-f838-4789-9c1f-8b7d1e0cf2e5)

# 使用帮助

​	图形化界面分为三个部分，左侧部分为数据库相关操作模块，中间为数据包、URL填写模块，右侧为杂项模块。

**左侧模块内容介绍**

- 测试级别：可选择1-5级，等级越高，SQL语句测试内容越多。
- 风险级别：可选择1-3级，1级采用相对安全的语法，3级采用非常危险的语法。
- 线程数：可选择1-20线程，通常SQLmap限制最高20线程。
- 当前数据库：执行--current-db命令，查看当前正在使用哪一个库。
- 当前用户：执行--current-user命令，查看正在使用的用户是哪一个。
- 当前用户DBA权限：执行--is-dba命令，查看当前用户是否是DBA权限。
- 枚举库名：执行--dbs命令，枚举所有库名。
- 枚举表名：执行--tables命令，需要填入指定库名，枚举指定库名下的所有表名。（不填写指定内容会枚举所有）
- 枚举列名：执行--columns命令，需要填入指定库名、指定表名，枚举指定库名、指定表名下的所有列名。（不填写指定内容会枚举所有）
- 枚举字段：执行--dump命令，需要填入指定库名、指定表名、指定列名，枚举指定库名、指定表名、指定列名下的所有字段。（不填写指定内容会枚举所有）
- 一键脱库：执行--dump-all命令，获取所有库名、表名、列名、字段并保存到文件中。
- OS交互式Shell：执行--os-shell命令。
- SQL交互式Shell：执行--sql-shell命令。
- 指定库名：执行-D命令。
- 指定表名：执行-T命令。
- 指定列名：执行-C命令。

**右侧模块内容介绍**

- 设置代理：格式为(http://|https://|socks5://IP:PORT)
- 代理身份验证：格式为(用户名:密码)
- 一键去特征：执行--random-agent--tamper=between--flush-session--randomize=1--skip=XSS命令。
- 打开所有优化开关：执行-o命令。
- 默认应答：执行--batch命令，使用默认的选项。
- 清除缓存：执行--purge命令，删除之前的记录缓存。
- 强制SSL通信：执行--force-ssl命令，强制sqlmap使用https进行请求。
- 批量扫描URL：执行-m命令，一行一条的形式填写URL。(中间文本框留空)
- 批量扫描数据包：使用前要在batch文件夹中放入txt文件，每一个txt文件对应一次扫描，循环执行-r命令，开启默认应答，启用大量cmd来运行，结束后自动打开sqlmap结果目录。(中间文本框留空)
- 注入方式：可选择指定注入方式或全部注入方式。
- 指定数据库类型：可选择指定数据库类型。
- 自定义参数：直接填写需要的额外参数，会自动添加在命令最后。
- 查看SQLMAP帮助：查看sqlmap-hh内容。
- 开始运行：保存中间内容并执行SQLmap命令。
- 文本框：回显运行的SQLmap命令。

**中间模块内容介绍**

- 中部文本框：填写http开头执行-u命令，填写数据包执行-r命令。

# 工具截图
![b9031b2470b1214f8752dd888dece118](https://github.com/honmashironeko/sqlmap-cn/assets/139044047/cdaf0648-21a1-48a5-9a0e-c5d3fa7ad820)
![02e83a5448761ef1d62de08b97c9a407](https://github.com/honmashironeko/sqlmap-cn/assets/139044047/30928bcf-d808-46ae-8769-00b0ebeb06af)
![6f0ec70cba8111660e4b8aad6998aa1e](https://github.com/honmashironeko/sqlmap-cn/assets/139044047/a302133e-7887-4112-98cc-b093c1349a3a)

# 最后一说

​	如果您方便的话，辛苦您为作者主页的个人项目点个star~ 并关注一下公众号：**樱花庄的本间白猫**

![Clip_2024-03-06_19-23-55](https://github.com/honmashironeko/sqlmap-cn/assets/139044047/ac76b86e-35b9-4c64-a00a-1eb7a7fe05d2)

​	如果出现bug或有建议，可以添加作者联系方式进行反馈！同时邀请进入交流群一起交流一下~

![e8273e81034a30640688127548f7f4b7](https://github.com/honmashironeko/sqlmap-cn/assets/139044047/1bd6390a-673c-42e6-9a62-074eb35e146e)
