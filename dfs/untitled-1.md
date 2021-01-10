# BitTorrent vs. IPFS

## BT和磁力是如何工作的？

BT简单说，就是一份文件被分成多个小块，当有人已经下载了某一个小块后，这个人可以成为除了数据源之外的另外的一个数据源，别人也可以从他这里下载，因此下载同一份的文件的人越多，下载的速度也就又可能越快。

但BT下载需要一个Tracker用以告诉大家谁已经下载了哪一块文件。如果这个Tracker down了的话，这个BT下载就不能进行。在BT的基础之上开发出了磁力下载，简单说就是每个人都可以成为Tracker（我的理解也可能不对~）。

回形针有一个很详细的讲解视频：

{% embed url="https://www.youtube.com/watch?v=jp0bF9Qu2Jw&ab\_channel=%E5%9B%9E%E5%BD%A2%E9%92%88PaperClip" %}

## BT和IPFS的区别

{% embed url="https://zhuanlan.zhihu.com/p/36787502" %}



从使用者的角度看，功能上来讲，主要有以下

1. 使用 BitTorrent 下载必须使用种子文件，将下载内容的所有地址放到这个种子文件中，才能下载。而 IPFS 使用 DAG 数据结构存储数据，下载任何文件时只需知道一个 hash 地址即可。
2. IPFS 的部分实现参考了分布式版本管理工具 git 的实现，因而它可以存储内容的多个版本，而 BitTorrent 是不支持这个功能的。
3. BitTorrent 下载必须使用种子文件，客户端只能下载种子文件内的内容，而 IPFS 不受这个限制，可以下载毫不相关的任何文件（当然是加密过的即使下下来如果没有密钥也是看不了的），于是 IPFS 内部的资源调度子模块 BitSwap 可以更高效地调度，预下载内容，从而提高下载效率。
4. 使用 IPFS 存储文件夹时，文件夹树形结构中的每个节点都有一个唯一的 hash, 因为可以只下载文件夹中的指定内容而无需下载整个文件夹。 BitTorrent 不支持这个功能。
5. BitTorrent 只是一个 download system， 而 IPFS 是一个 filesystem，意味着你可以将 IPFS mount 到你的本地电脑然后当磁盘一样操作。



