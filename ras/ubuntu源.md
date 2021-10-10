https://blog.csdn.net/qq_16547997/article/details/106793339

树莓派4B安装Ubuntu20.04 解决更换镜像源问题

chenshuichuan 2020-06-16 19:07:10  8197  收藏 47
文章标签： ubuntu
版权
树莓派4B安装Ubuntu20.04 参考 https://www.bilibili.com/video/BV1AC4y1x7hz/?spm_id_from=333.788.videocard.0

由于没仔细看，在安装成功后更改国内镜像源时使用了x86架构的镜像源如阿里源：http://mirrors.aliyun.com/ubuntu

清华源：https://mirrors.tuna.tsinghua.edu.cn/ubuntu/

都导致了sudo apt-get update 时出现错误E: Some index files failed to download, they have been ignored, or old ones used instead

最后发现中科大镜像源的说明：：http://mirrors.ustc.edu.cn/help/ubuntu-ports.html

所以树莓派4B的架构要用的是ubuntu-ports的源，而不是ubuntu 的源

整理后的源 /etc/apt/sources.list文件

## 如出现无法安全的用该源进行更新,则将https换为http

# 默认注释了源码仓库，如有需要可自行取消注释
deb https://mirrors.ustc.edu.cn/ubuntu-ports/ focal main restricted universe multiverse
# deb-src https://mirrors.ustc.edu.cn/ubuntu-ports/ focal main main restricted universe multiverse
deb https://mirrors.ustc.edu.cn/ubuntu-ports/ focal-updates main restricted universe multiverse
# deb-src https://mirrors.ustc.edu.cn/ubuntu-ports/ focal-updates main restricted universe multiverse
deb https://mirrors.ustc.edu.cn/ubuntu-ports/ focal-backports main restricted universe multiverse
# deb-src https://mirrors.ustc.edu.cn/ubuntu-ports/ focal-backports main restricted universe multiverse
deb https://mirrors.ustc.edu.cn/ubuntu-ports/ focal-security main restricted universe multiverse
# deb-src https://mirrors.ustc.edu.cn/ubuntu-ports/ focal-security main restricted universe multiverse