# 云监控中inode使用率监控具体作用是什么 {#concept_tmz_r54_zdb .concept}

本文为您介绍云监控中inode使用率监控的具体作用。

在Linux/Unix系统内部，不是使用文件名，而是使用inode号码来识别文件。对于系统来说，文件名只是inode号码便于识别的别称或者绰号。

表面上，用户通过文件名，打开文件。实际上，系统内部这个过程分成三步：

1.  系统找到这个文件名对应的inode号码；
2.  通过inode号码，获取inode信息；
3.  根据inode信息，找到文件数据所在的block，读出数据。

由于每个文件都必须有一个inode，因此有可能发生inode已经用光，但是硬盘还未存满的情况。这时，就无法在硬盘上创建新文件，这就是此监控项的目的。

查看每个硬盘分区的inode总数和已经使用的数量，可以使用`df -i`。

如果要查看每个inode节点的大小，可以用`sudo dumpe2fs -h /dev/hda | grep "Inode size"`。

