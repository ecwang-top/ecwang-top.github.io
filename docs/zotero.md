# 文献管理软件Zotero推荐

[Zotero](https://www.zotero.org/)是开源的文献管理软件, 和它类似的竟品有endnote, mendeley等.
最近随着Zotero 7.0的更新, Zotero已经变的相当好用了. 
它能够实现的功能包括直接从网页保存文献到文献库并自动下载pdf, 在pdf中做标记和笔记, 通过插件可以实现划词翻译, 十分方便.

## 安装

进入这个网址[(https://www.zotero.org/download)](https://www.zotero.org/download), 可以下载你的操作系统对应的Zotero 7应用程序(Windows/MacOS/Linux).
此外还会提示你安装Zotero Connector, 这是一个浏览器插件, 你可以在你常用的浏览器上安装这个插件, 用它可以从文献的网址直接保存到你的Zotero文献库.

## 如何把文件保存到库?

大概有两种方式:
- 通过Zotero Connector插件: 在文献的网址(例如ihttps://ui.adsabs.harvard.edu/abs/2024ApJ...971L..14M/abstract, https://arxiv.org/abs/2408.15214, etc.), 点击Zotero Connector的图标或者设置的快捷键(如Alt+Z/Opt+Z), 随后可以选择保存到什么路径; 程序会自动查找可用的pdf并保存.
- 直接把pdf文件拖到Zotero的窗口里, 程序会根据pdf文件的meta data获取文献的信息并创建条目.

> 如果保存了条目以后没有自动保存pdf, 可以进入设置里面检查一下: 
> 编辑 -> 设置 -> 常规 -> 文件处理 -> 勾选"保存条目时自动附加相关的PDF文档及其他文件"以及"自动检索PDF和电子书的元数据"

## 划词翻译插件

非常实用的功能. 在[(https://github.com/windingwind/zotero-pdf-translate)](https://github.com/windingwind/zotero-pdf-translate)页面找到"Releases"并点击进入, 下载最新的"translate-for-zotero.xpi".

然后在Zotero界面的选项中选择工具 -> 插件 -> (齿轮符号) -> "Install Plugin From File", 找到刚才下载的.xpi文件并确认安装.

在编辑 -> 设置 -> 翻译中调整设置: 我建议把"翻译服务"设置为DeepLX(不带API那个), 比其他的快(其他的也可以试试). 
其他设置自己酌情调整即可.

## 做笔记

在看文献时, 可能会发现有一些想要用自己的话总结的笔记, 这时候要是把笔记记到别的地方可能将来不是很好找; 
但是在Zotero 7中, 在浏览文献pdf的窗口右侧边栏, 点击黄色的"笔记"图标, 点击"条目笔记"即可直接编辑条目笔记.
这个笔记是和文献库中的这个条目绑定的, 将来会很容易查找. 
笔记基本支持markdown语法, 很方便.

## 多设备同步

如果你有台式机和笔记本, 再或者想在iPad, 手机上(认真的?)看文献(手机上也可以下载zotero), 同步功能就显得十分重要了. 
官方提供的同步功能只包括条目的同步, 如果想要同步pdf文件的标注就需要付费了. 
好在我们可以通过WebDAV服务利用第三方网盘克服这一点. 下面简单说一下步骤:

- 首先打开编辑 -> 设置 -> 同步, 在"数据同步"中注册一个zotero账号, 这个只是用来同步条目元数据, 不花钱的.
- 注册一个[坚果云](https://www.jianguoyun.com/)账号(他们的服务免费很好用)
- 登录坚果云之后, 点击网页右上角的"自己的用户名" -> 账户信息 -> 安全选项 -> 第三方应用管理 -> 添加应用, 这里随便起个名字然后复制他给出的密码(只会显示一次, 可以复制粘贴到一个txt文档里).
- 回到Zotero的设置 -> 同步 -> 文件同步, 将"我的文库"附件同步方式选择为"WebDAV". 网址选择"https", 后面框里输入"dav.jianguoyun.com/dav", 用户名是你坚果云账号的注册邮箱, 密码是刚才复制的密码, 点击"验证服务器".

就可以同步PDF文件了.


## 文献分类

右键点击"我的文库", 可以"新建分类", 这样就可以分类管理你的文献.

## 订阅arxiv更新

右键点击"订阅", 新建订阅, 导入网址(http://arxiv.org/rss/astro-ph.GA)即可每天自动在这里更新astro-ph.GA分类下的新文章.
在这个页面中, 可以查看文章的标题, 如果想要看摘要可以右键点击条目并在线查看. 
如果看到感兴趣的文章想要仔细看, 可以"添加到我的文库", 指定一个分类并导入, 这样这篇文献就导入了你的文库并自动下载了pdf.

## 导出bibtex

用latex写文章进行引用的时候, 用文献管理软件可以方便地导出包含所有文献的bibtex文件. 这里推荐下载插件[zotero-better-bibtex](https://github.com/retorquere/zotero-better-bibtex), 安装过程和安装zotero-pdf-translate的完全一致,不再赘述.

Updating... 作者: 于浩然 最后修改日期:24.08.28
