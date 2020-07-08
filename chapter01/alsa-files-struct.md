# ALSA 文件结构

ALSA中的firmware部分已经集成到linux内核中(linux/sound/目录)中，整个ALSA项目的文件结构如下:

- alsa-driver
    运行在内核态的alsa部门分，也包含一小部分运行在用户态的部分，包括一些启动脚本以及头文件。由于目前的linux内核已经默认集成了alsa，
    所以这个库目前已经废止了，不过老的库仍然可用。
- alsa-lib
    开发者编译应用需要的用户态的库
- alsa-utils
    包含通用的命令行工具比如aplay,arecord,amixer
- alsa-tools
    包含一些不常用的工具
- alsa-firmware
    内核驱动，包含各种各样的三方驱动的二进制驱动。
- alsa-plugins
    包含各种用到的插件，比如jack, pulse 等
- alsa-oss
    包括OSS兼容层
- pyalsa
    alsa-lib的python包装,可用python调用alsa接口


ALSA用户态的内容主要都在alsa-lib库中完成，内核的代码已经集成在Linux内核中，主要在`linux/asound/`目录。
理解ALSA的流程主要是熟悉alsa-lib库以及内核中的部分。
