# wmt_xv6_study
[WIP] My xv6 document and sources study, based on jamesrxian/xv6-chinese

## References
* https://github.com/jamesrxian/xv6-chinese/tree/rev9
* https://github.com/weimingtom/wmt_ai_study/blob/master/os_001.md
* xv6-chinese-rev9_chrome.pdf  
* use vscode plugins to print, see https://blog.csdn.net/m0_68997646/article/details/128612630  

## xv6 中文文档, 行号对应的版本为rev7
update 02/25/2016

2014 版的 xv6 (rev8) 相关文档正在翻译中，详见 `rev8` 分支。

xv6 是 MIT 开发的一个教学用的完整的类 Unix 操作系统，并且在 MIT 的操作系统课程 6.828, http://pdos.csail.mit.edu/6.828/2012/xv6.html 中使用。通过阅读并理解 xv6 的代码，可以清楚地了解操作系统中众多核心的概念，对操作系统感兴趣的同学十分推荐一读！这份文档是中文翻译的 MIT xv6 文档，是阅读代码过程中非常好的参考资料。

原文在此, http://pdos.csail.mit.edu/6.828/2012/xv6/book-rev7.pdf

文中引用的 xv6 源代码, http://pdos.csail.mit.edu/6.828/2012/xv6/xv6-rev7.pdf

强烈推荐 xv6 源代码同本书一同阅读！原作和翻译中遇到的括号内的数字，都是指上面链接中文件的源代码行号。

同时，我们的翻译文档也可以通过 gitbook, https://www.gitbook.io/book/th0ar/xv6-chinese 阅读  

## 译者

* 鲜染 北京大学 信息科学技术学院 计算机系
* 赵天雨 北京大学 信息科学技术学院 计算机系
* 胡树伟 北京大学 信息科学技术学院 计算机系（I guess）
* 胡文涛 KAUST CS
* 曹扬 上海交通大学 电子信息与电气工程学院 计算机系
* 安润功 中国人民大学

*如果你愿意贡献，你的名字也会出现在这里！*

## 许可证（License）

文档中涉及到的 xv6 源代码使用 MIT, http://www.opensource.org/licenses/mit-license.php 许可证。中文翻译使用 GNU GPL V3.0, http://www.gnu.org/copyleft/gpl.html 许可证，在 GNU GPL V3.0 之上，转载和引用须注明本项目 Github 地址。

## 目录, 总结  
* 封面
* 前言
* 第零章 操作系统接口
* 第一章 第一个进程
* 第二章 页表
* 第三章 陷入，中断和驱动程序
* 第四章 锁
* 第五章 调度
* 第六章 文件系统
* 附录A PC 硬件
* 附录B 引导加载器
* 术语
* 勘误

## 封面
**xv6**

一个简单， 类 Unix 的教学操作系统

Russ Cox

Frans Kasshoek

Robert Morris

xv6-book@pdos.csail.mit.edu

翻译：

鲜染

xianran@pku.edu.cn

赵天雨

zhaoty.ting@gmail.com

2013年国庆

### 前言和致谢

这是一份为操作系统课编写的教学草案。它通过研究一个名为 xv6 的操作系统内核来解释操作系统中的主要概念。xv6 是 Dennis Ritchie 和 Ken Thompson 合著的 Unix Version 6（v6）操作系统的重新实现。xv6 在一定程度上遵守 v6 的结构和风格，但它是用 ANSI C 实现的，并且是基于 x86 多核处理器的。

这本教材应该和 xv6 源代码一起阅读，这是 John Lion 在 Unix 6th Edition（Peer to Peer Communications；ISBN：1-57398-013-7；第一版（2000年7月14日）的评注中推荐的学习方式。 参见[http://pdos.csail.mit.edu/6.828](http://pdos.csail.mit.edu/6.828) 上有关于 v6 和 xv6 的资料。

我们已经在 6.828 —— MIT 的操作系统课程中使用了这本教材。我们向参与 6.828 的教职员工、助教和学生表示感谢，他们都直接或间接向 xv6 做出了贡献。此处我们要特别感谢 Austin Clements 和 Nicholai Zeldovich。
