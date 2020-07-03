---
description: An introduction to ALSA project
---

# ALSA 入门介绍

最近几个月调试ALSA的总结。写这个文档的主要原因是网络上能搜到的资料有限且过时，包括官方介绍文档。

介绍采用自顶向下的方式，即先讲解如何使用API，再去介绍ALSA的整体框架，以及数据流如何从用户态最终传递到内核态，最终与codec交互。



