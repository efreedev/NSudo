NSudo - A Powerful System Administration Tool
========================================================================================

本工具是raymai97的超级命令提示符那篇文章里所说的景友制作的单文件版的下一版本

感谢raymai97，他写的”[分享] 超级命令提示符 让你拥有真正的最高权限“给我以很大启发（他甚至还留下了源代码给我们研究，我真的很钦佩他）

我通过他的源代码，把源代码合二为一；并且删掉重复的部分；这样就可以使用一个文件就可以直接打开TrustedInstaller权限的命令提示符了

下面引用raymai97的原文介绍一下TrustedInstaller

========================================================================================
TrustedInstaller是Windows Update等系统组件需要修改文件时，使用的“代理”。

TI的权限非常高~ 比SYSTEM还要高~ 堪称Windows版的ROOT权限~

TI模式的CMD可以让你在不修改/破坏NTFS权限设置下，直接对系统文件进行操作，比如替换、重命名、删除…… 已验证可以成功修改的文件包括explorer.exe、shell32.exe、iexplore.exe。

使用TI模式的CMD，启动的程序也会自动有TI权限。因此你可以用它启动你喜欢的第三方文件管理器，比如7zFM。要注意的是，explorer不支持TI模式，它将无法正常运行。

你也许会想问，修改NTFS权限设置不就好了？网上有很多“一键更改所有者”“一键获得权限”呢~

要知道，NTFS权限设置是用来防止你系统文件被瞎改的。绝大多数人往往在修改权限和文件后，没有恢复权限设置，因此以后其它程序都可以直接对这些文件进行修改！

如果是默认的NTFS权限设置，即使是以管理员身份运行的程序，也需要使用相当多的代码来让自己拥有权限，修改相关文件。

Win8的WindowsApps文件夹是一个典型的例子。如果你修改权限后，没有改回去，就会有打不开Apps（闪退）的风险，严重者会所有Apps都开不到！

好吧，你说你要手动改权限，然后修改文件，再把权限改回去…… 试想想，就为了修改一个系统文件，就这样麻烦了。如果有多个系统文件呢？

因此我认为，直接使用具有TI权限的CMD，再搭配其它第三方文件管理器（比如7zFM），会比修改NTFS权限设置来得方便、快速、安全~

========================================================================================

改进日志

NSudo 2.1
1.实现自动开启所有权限Token
2.对cmd的调用使用绝对路径，估计可以避免一些不必要的Bug
3.优化程序代码

NSudo 2.0
1.代码全部使用C++ Win32 SDK重写（程序从692KB缩小到92KB）
2.提供获取权限的选项
3.提供命令行参数模式
4.更换了图标

NTIShell 1.0
根据raymai97的超级命令提示符制作的第一个版本

使用方法：双击NSudo.exe根据提示操作即可

压缩包在附件（源代码也在里面……）
