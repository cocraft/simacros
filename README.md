# simacros
simarcros支持 Source Insight 3.5 and 4.0 宏定义，提高开发效率和代码浏览

# 目录说明

chnChar.em：si4.0以下中文支持
quicker.em：该文件提高编码效率宏定义
codeReview.em：该文件主要解决了在项目开发过程中或者在质量部组织的代码飞检活动中评审人统计代码缺陷并提交代码作者进行缺陷确认修改，之后再提交给评审人进行问题修改确认的活动。
doc：详细文档

# 配置说明
## Source Insight
如果已经存在Base工程，可以直接将quicker.em加入到其中，并且同步文件。也可以删除它重建立一个Base工程，然后再把quicker.em加入其中，同步工程后，再定义好热键和菜单
config_si30.CF3是si3.x的配置文件，config_si40.xml是si4.x的配置文件，它已经定义好菜单和热键。图方便的话可以直接使用这两个配置文件，这样就可以不用自己定义菜单和热键了。
选择Options的Save Configuration先保存自己的配置，以便回退，然后再选择Options的
Load Configuration来装载该配置，如果不喜欢我的配置风格，只想要热键和菜单定义，
只要勾上菜单和热键两个子项即可。

1.运行Source Insight，打开Base工程，如果没有该工程，则生成它，将quicker.em、codeReview.em等em文件加入到工程中
2.安装触发热键和菜单，打开SI的Options的Key Assignments菜单，在Command窗口中选择AutoExpand，然后对其赋一个热键，例如Ctrl+Enter
3.对于FormatLine,UpdateFunctionList,InsertTraceInfo,InsertFuncName,ReplaceBufTab,ReplaceTabInProj,ComentCPPtoC等功能，可以根据情况定义为菜单或热键
4.quicker有两种命令，一种是扩展命令，一种是普通命令。扩展命令：在代码文件中输入命令名，然后按前面AutoExpand宏所定义的热键（Ctrl+Enter）来执行该命令，对于块命令输入命令后再选择输入块 普通命令：直接根据定义的热键或菜单来执行，目前一般的扩展命令都对应有相应的普通命令