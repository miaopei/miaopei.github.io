---
title: 值得推荐的C/C++框架和库
tags: c/c++
reward: true
categories: c/c++
toc: true
abbrlink: 39639
description: Webbench是一个在linux下使用的非常简单的网站压测工具。它使用fork()模拟多个客户端同时访问我们设定的URL，测试网站在压力下工作的性能，最多可以模拟3万个并发连接去测试网站的负载能力。Webbench使用C语言编写, 代码实在太简洁，源码加起来不到600行。
date: 2018-06-08 10:14:50
---

## 1. 值得学习的 C 语言开源项目

### 1.1 Libev

libev 是一个开源的事件驱动库，基于 epoll，kqueue 等 OS 提供的基础设施。其以高效出名，它可以将 IO 事件，定时器，和信号统一起来，统一放在事件处理这一套框架下处理。基于 Reactor 模式，效率较高，并且代码精简（4.15 版本 8000 多行），是学习事件驱动编程的很好的资源。

<!-- more -->

下载链接：http://software.schmorp.de/pkg/libev.html

### 1.2 Memcached

Memcached 是一个高性能的分布式内存对象缓存系统，用于动态 Web 应用以减轻数据库负载。它通过在内存中缓存数据和对象来减少读取数据库的次数，从而提供动态数据库驱动网站的速度。Memcached 基于一个存储键 / 值对的 hashmap。Memcached-1.4.7 的代码量还是可以接受的，只有 10K 行左右。

下载地址：http://memcached.org/

### 1.3 Redis

Redis 是一个使用 C 语言写成的，开源的 key-value 数据库。Redis 支持的操作和数据类型比 Memcached 要多，现在主要用于缓存，支持主从同步机制，Redis 的学习可以参考 <<Redis 设计与实现>> 一书。

下载地址：http://redis.io/

### 1.4 Webbench

Webbench 是一个在 linux 下使用的非常简单的网站压测工具。它使用 fork () 模拟多个客户端同时访问我们设定的 URL，测试网站在压力下工作的性能，最多可以模拟 3 万个并发连接去测试网站的负载能力。Webbench 使用 C 语言编写，代码实在太简洁，源码加起来不到 600 行。

下载链接：[https://github.com/LippiOuYang/WebBenchl](https://github.com/LippiOuYang/WebBench)

### 1.5 APR（Apache Portable Runtime）

这是由 Apache 社区维护的 C 开源库，主要提供操作系统相关的功能（文件系统、进程、线程、用户、IPC）。此外还提供了一些网络相关的功能。

APR 原先是 Apache Web 服务器的一个组成部分，后来独立出来，成为一个单独的开源项目。
主页：[https://apr.apache.org](https://apr.apache.org/)

### 1.6 Tinyhttpd

tinyhttpd 是一个超轻量型 Http Server，使用 C 语言开发，全部代码只有 502 行 (包括注释)，附带一个简单的 Client，可以通过阅读这段代码理解一个 Http Server 的本质。

下载链接：https://github.com/LippiOuYang/Tinyhttpd

### 1.7 cJSON

cJSON 是 C 语言中的一个 JSON 编解码器，非常轻量级，C 文件只有 500 多行，速度也非常理想。

cJSON 也存在几个弱点，虽然功能不是非常强大，但 cJSON 的小身板和速度是最值得赞赏的。其代码被非常好地维护着，结构也简单易懂，可以作为一个非常好的 C 语言项目进行学习。

项目主页:http://sourceforge.net/projects/cjson/

### 1.8 CMockery

cmockery 是 google 发布的用于 C 单元测试的一个轻量级的框架。它很小巧，对其他开源包没有依赖，对被测试代码侵入性小。cmockery 的源代码行数不到 3K，你阅读一下 will_return 和 mock 的源代码就一目了然了。

主要特点：

- 免费且开源，google 提供技术支持；
- 轻量级的框架，使测试更加快速简单；
- 避免使用复杂的编译器特性，对老版本的编译器来讲，兼容性好；
- 并不强制要求待测代码必须依赖 C99 标准，这一特性对许多嵌入式系统的开发很有用

下载链接：http://code.google.com/p/cmockery/downloads/list

### 1.9 Lua

Lua 很棒，Lua 是巴西人发明的，这些都令我不爽，但是还不至于脸红，最多眼红。

让我脸红的是 Lua 的源代码，百分之一百的 ANSI C，一点都不掺杂。在任何支持 ANSI C 编译器的平台上都可以轻松编译通过。我试过，真是一点废话都没有。Lua 的代码数量足够小，5.1.4 仅仅 1.5W 行，去掉空白行和注释估计能到 1W 行。

下载地址：http://www.lua.org/

### 1.10 SQLite

SQLite 是一个开源的嵌入式关系数据库，实现自包容、零配置、支持事务的 SQL 数据库引擎。 其特点是高度便携、使用方便、结构紧凑、高效、可靠。足够小，大致 3 万行 C 代码，250K。

下载地址：http://www.sqlite.org/ 。

### 1.11 UNIX v6

UNIX V6 的内核源代码包括设备驱动程序在内 约有 1 万行，这个数量的源代码，初学者是能够充分理解的。有一种说法是一个人所能理解的代码量上限为 1 万行，UNIX V6 的内核源代码从数量上看正好在这个范围之内。看到这里，大家是不是也有 “如果只有 1 万行的话没准儿我也能学会” 的想法呢？

另一方面，最近的操作系统，例如 Linux 最新版的内核源代码据说超过了 1000 万行。就算不是初学者，想完全理解全部代码基本上也是不可能的。

下载地址：http://minnie.tuhs.org/cgi-bin/utree.pl?file=V6

### 1.12 NETBSD

NetBSD 是一个免费的，具有高度移植性的 UNIX-like 操作系统，是现行可移植平台最多的操作系统，可以在许多平台上执行，从 64bit alpha 服务器到手持设备和嵌入式设备。NetBSD 计划的口号是：”Of course it runs NetBSD”。它设计简洁，代码规范，拥有众多先进特性，使得它在业界和学术界广受好评。由于简洁的设计和先进的特征，使得它在生产和研究方面，都有卓越的表现，而且它也有受使用者支持的完整的源代码。许多程序都可以很容易地通过 NetBSD Packages Collection 获得。

下载地址：http://www.netbsd.org/

## 2. C++ 资源大全

关于 C++ 框架、库和资源的一些汇总列表，内容包括：标准库、Web 应用框架、人工智能、数据库、图片处理、机器学习、日志、代码分析等。

### 2.1 标准库

C++ 标准库，包括了 STL 容器，算法和函数等。

- [C++ Standard Library](http://en.wikipedia.org/wiki/C%2B%2B_Standard_Library)：是一系列类和函数的集合，使用核心语言编写，也是 C++ISO 自身标准的一部分。
- [Standard Template Library](http://en.wikipedia.org/wiki/Standard_Template_Library)：标准模板库
- [C POSIX library](http://en.wikipedia.org/wiki/C_POSIX_library) ： POSIX 系统的 C 标准库规范
- [ISO C++ Standards Committee](https://github.com/cplusplus) ：C++ 标准委员会

### 2.2 框架

C++ 通用框架和库

- [Apache C++ Standard Library](http://stdcxx.apache.org/)：是一系列算法，容器，迭代器和其他基本组件的集合
- [ASL](http://stlab.adobe.com/) ：Adobe 源代码库提供了同行的评审和可移植的 C++ 源代码库。
- [Boost](https://github.com/boostorg) ：大量通用 C++ 库的集合。
- [BDE](https://github.com/bloomberg/bde) ：来自于彭博资讯实验室的开发环境。
- [Cinder](http://libcinder.org/)：提供专业品质创造性编码的开源开发社区。
- [Cxxomfort](http://ryan.gulix.cl/fossil.cgi/cxxomfort/)：轻量级的，只包含头文件的库，将 C++ 11 的一些新特性移植到 C++03 中。
- [Dlib](http://dlib.net/)：使用契约式编程和现代 C++ 科技设计的通用的跨平台的 C++ 库。
- [EASTL](https://github.com/paulhodge/EASTL) ：EA-STL 公共部分
- [ffead-cpp](https://github.com/sumeetchhetri/ffead-cpp) ：企业应用程序开发框架
- [Folly](https://github.com/facebook/folly)：由 Facebook 开发和使用的开源 C++ 库
- [JUCE](https://github.com/julianstorer/JUCE) ：包罗万象的 C++ 类库，用于开发跨平台软件
- [libPhenom](https://github.com/facebook/libphenom)：用于构建高性能和高度可扩展性系统的事件框架。
- [LibSourcey](https://github.com/sourcey/libsourcey) ：用于实时的视频流和高性能网络应用程序的 C++11 evented IO
- [LibU](https://github.com/koanlogic/libu) ： C 语言写的多平台工具库
- [Loki](http://loki-lib.sourceforge.net/) ：C++ 库的设计，包括常见的设计模式和习语的实现。
- [MiLi](https://code.google.com/p/mili/) ：只含头文件的小型 C++ 库
- [openFrameworks](http://www.openframeworks.cc/) ：开发 C++ 工具包，用于创意性编码。
- [Qt](http://qt-project.org/) ：跨平台的应用程序和用户界面框架
- [Reason](http://code.google.com/p/reason/) ：跨平台的框架，使开发者能够更容易地使用 Java，.Net 和 Python，同时也满足了他们对 C++ 性能和优势的需求。
- [ROOT](http://root.cern.ch/) ：具备所有功能的一系列面向对象的框架，能够非常高效地处理和分析大量的数据，为欧洲原子能研究机构所用。
- [STLport](http://www.stlport.org/)：是 STL 具有代表性的版本
- [STXXL](http://stxxl.sourceforge.net/)：用于额外的大型数据集的标准模板库。
- [Ultimate++](http://www.ultimatepp.org/) ：C++ 跨平台快速应用程序开发框架
- [Windows Template Library](http://sourceforge.net/projects/wtl/)：用于开发 Windows 应用程序和 UI 组件的 C++ 库
- [Yomm11](https://github.com/jll63/yomm11) ：C++11 的开放 multi-methods.

### 2.3 人工智能

- [btsk](https://github.com/aigamedev/btsk) ：游戏行为树启动器工具
- [Evolving Objects](http://eodev.sourceforge.net/)：基于模板的，ANSI C++ 演化计算库，能够帮助你非常快速地编写出自己的随机优化算法。
- [Neu](https://github.com/andrometa/neu)：C++11 框架，编程语言集，用于创建人工智能应用程序的多用途软件系统。

### 2.4 异步事件循环

- [Boost.Asio](http://think-async.com/)：用于网络和底层 I/O 编程的跨平台的 C++ 库。
- [libev](http://libev.schmorp.de/) ：功能齐全，高性能的时间循环，轻微地仿效 libevent，但是不再像 libevent 一样有局限性，也修复了它的一些 bug。
- [libevent](http://libevent.org/) ：事件通知库
- [libuv](https://github.com/joyent/libuv) ：跨平台异步 I/O。

### 2.5 音频

音频，声音，音乐，数字化音乐库

- [FMOD](http://www.fmod.org/) ：易于使用的跨平台的音频引擎和音频内容的游戏创作工具。
- [Maximilian](https://github.com/micknoise/Maximilian) ：C++ 音频和音乐数字信号处理库
- [OpenAL](http://www.openal.org/) ：开源音频库 — 跨平台的音频 API
- [Opus](http://opus-codec.org/)：一个完全开放的，免版税的，高度通用的音频编解码器
- [Speex](http://www.speex.org/)：免费编解码器，为 Opus 所废弃
- [Tonic](https://github.com/TonicAudio/Tonic)： C++ 易用和高效的音频合成
- [Vorbis](http://xiph.org/vorbis/)： Ogg Vorbis 是一种完全开放的，非专有的，免版税的通用压缩音频格式。

### 2.6 生态学

生物信息，基因组学和生物技术

- [libsequence](http://molpopgen.github.io/libsequence/)：用于表示和分析群体遗传学数据的 C++ 库。
- [SeqAn](http://www.seqan.de/)：专注于生物数据序列分析的算法和数据结构。
- [Vcflib](https://github.com/ekg/vcflib) ：用于解析和处理 VCF 文件的 C++ 库
- [Wham](https://github.com/jewmanchue/wham)：直接把联想测试应用到 BAM 文件的基因结构变异。

### 2.7 压缩

压缩和归档库

- [bzip2](http://www.bzip.org/)：一个完全免费，免费专利和高质量的数据压缩
- [doboz](https://bitbucket.org/attila_afra/doboz/overview)：能够快速解压缩的压缩库
- [PhysicsFS](https://icculus.org/physfs/)：对各种归档提供抽象访问的库，主要用于视频游戏，设计灵感部分来自于 Quake3 的文件子系统。
- [KArchive](https://projects.kde.org/projects/frameworks/karchive)：用于创建，读写和操作文件档案（例如 zip 和 tar）的库，它通过 QIODevice 的一系列子类，使用 gzip 格式，提供了透明的压缩和解压缩的数据。
- [LZ4](https://code.google.com/p/lz4/) ：非常快速的压缩算法
- [LZHAM](https://code.google.com/p/lzham/) ：无损压缩数据库，压缩比率跟 LZMA 接近，但是解压缩速度却要快得多。
- [LZMA](http://www.7-zip.org/sdk.html) ：7z 格式默认和通用的压缩方法。
- [LZMAT](http://www.matcode.com/lzmat.htm) ：及其快速的实时无损数据压缩库
- [miniz](https://code.google.com/p/miniz/)：单一的 C 源文件，紧缩 / 膨胀压缩库，使用 zlib 兼容 API，ZIP 归档读写，PNG 写方式。
- [Minizip](https://github.com/nmoinvaz/minizip)：Zlib 最新 bug 修复，支持 PKWARE 磁盘跨越，AES 加密和 IO 缓冲。
- [Snappy](https://code.google.com/p/snappy/) ：快速压缩和解压缩
- [ZLib](http://zlib.net/) ：非常紧凑的数据流压缩库
- [ZZIPlib](http://zziplib.sourceforge.net/)：提供 ZIP 归档的读权限。

### 2.8 并发性

并发执行和多线程

- [Boost.Compute](https://github.com/kylelutz/compute) ：用于 OpenCL 的 C++GPU 计算库
- [Bolt](https://github.com/HSA-Libraries/Bolt) ：针对 GPU 进行优化的 C++ 模板库
- [C++React](https://github.com/schlangster/cpp.react) ：用于 C++11 的反应性编程库
- [Intel TBB](https://www.threadingbuildingblocks.org/) ：Intel 线程构件块
- [Libclsph](https://github.com/libclsph/libclsph)：基于 OpenCL 的 GPU 加速 SPH 流体仿真库
- [OpenCL](https://www.khronos.org/opencl/) ：并行编程的异构系统的开放标准
- [OpenMP](http://openmp.org/)：OpenMP API
- [Thrust](http://thrust.github.io/) ：类似于 C++ 标准模板库的并行算法库
- [HPX](https://github.com/STEllAR-GROUP/hpx/) ：用于任何规模的并行和分布式应用程序的通用 C++ 运行时系统
- [VexCL](https://github.com/ddemidov/vexcl) ：用于 OpenCL/CUDA 的 C++ 向量表达式模板库。

### 2.9 容器

- [C++ B-tree](https://code.google.com/p/cpp-btree/) ：基于 B 树数据结构，实现命令内存容器的模板库
- [Hashmaps](https://github.com/goossaert/hashmap)： C++ 中开放寻址哈希表算法的实现

### 2.10 密码学

- [Bcrypt](http://bcrypt.sourceforge.net/) ：一个跨平台的文件加密工具，加密文件可以移植到所有可支持的操作系统和处理器中。
- [BeeCrypt](https://github.com/fffaraz/awesome-cpp/blob/master)：
- [Botan](http://botan.randombit.net/)： C++ 加密库
- [Crypto++](http://www.cryptopp.com/)：一个有关加密方案的免费的 C++ 库
- [GnuPG](https://www.gnupg.org/)： OpenPGP 标准的完整实现
- [GnuTLS](http://www.gnutls.org/) ：实现了 SSL，TLS 和 DTLS 协议的安全通信库
- [Libgcrypt](http://www.gnu.org/software/libgcrypt/)
- [libmcrypt](https://github.com/fffaraz/awesome-cpp/blob/master)
- [LibreSSL](http://www.libressl.org/)：免费的 SSL/TLS 协议，属于 2014 OpenSSL 的一个分支
- [LibTomCrypt](https://github.com/libtom/libtomcrypt)：一个非常全面的，模块化的，可移植的加密工具
- [libsodium](https://github.com/jedisct1/libsodium)：基于 NaCI 的加密库，固执己见，容易使用
- [Nettle](http://www.lysator.liu.se/~nisse/nettle/) 底层的加密库
- [OpenSSL](http://www.openssl.org/) ： 一个强大的，商用的，功能齐全的，开放源代码的加密库。
- [Tiny AES128 in C](https://github.com/kokke/tiny-AES128-C) ：用 C 实现的一个小巧，可移植的实现了 AES128ESB 的加密算法

### 2.11 数据库

数据库，SQL 服务器，ODBC 驱动程序和工具

- [hiberlite](https://github.com/paulftw/hiberlite) ：用于 Sqlite3 的 C++ 对象关系映射
- [Hiredis](https://github.com/redis/hiredis)： 用于 Redis 数据库的很简单的 C 客户端库
- [LevelDB](https://github.com/google/leveldb)： 快速键值存储库
- [LMDB](http://symas.com/mdb/)：符合数据库四大基本元素的嵌入键值存储
- [MySQL++](http://www.tangentsoft.net/mysql++/)：封装了 MySql 的 C API 的 C++ 包装器
- [RocksDB](https://github.com/facebook/rocksdb)：来自 Facebook 的嵌入键值的快速存储
- [SQLite](http://www.sqlite.org/)：一个完全嵌入式的，功能齐全的关系数据库，只有几百 KB，可以正确包含到你的项目中。

### 2.12 调试

调试库， 内存和资源泄露检测，单元测试

- [Boost.Test](http://www.boost.org/doc/libs/master/libs/test/doc/html/index.html)：Boost 测试库
- [Catch](https://github.com/philsquared/Catch)：一个很时尚的，C++ 原生的框架，只包含头文件，用于单元测试，测试驱动开发和行为驱动开发。
- [CppUnit](http://www.freedesktop.org/wiki/Software/cppunit/)：由 JUnit 移植过来的 C++ 测试框架
- [CTest](http://www.cmake.org/cmake/help/v2.8.8/ctest.html)：CMake 测试驱动程序
- [googletest](http://code.google.com/p/googletest/)：谷歌 C++ 测试框架
- [ig-debugheap](https://github.com/deplinenoise/ig-debugheap)：用于跟踪内存错误的多平台调试堆
- [libtap](https://github.com/zorgnax/libtap)：用 C 语言编写测试
- [MemTrack](http://www.almostinfinite.com/memtrack.html) — 用于 C++ 跟踪内存分配
- [microprofile](https://bitbucket.org/jonasmeyer/microprofile/overview)- 跨平台的网络试图分析器
- [minUnit](http://www.jera.com/techinfo/jtns/jtn002.html) ：使用 C 写的迷你单元测试框架，只使用了两个宏
- [Remotery](https://github.com/Celtoys/Remotery)：用于 web 视图的单一 C 文件分析器
- [UnitTest++](http://unittest-cpp.sourceforge.net/)：轻量级的 C++ 单元测试框架

### 2.13 游戏引擎

- [Cocos2d-x](http://www.cocos2d-x.org/) ：一个跨平台框架，用于构建 2D 游戏，互动图书，演示和其他图形应用程序。
- [Grit](http://gritengine.com/) ：社区项目，用于构建一个免费的游戏引擎，实现开放的世界 3D 游戏。
- [Irrlicht](http://irrlicht.sourceforge.net/) ：C++ 语言编写的开源高性能的实时 #D 引擎
- [Polycode](http://polycode.org/)：C++ 实现的用于创建游戏的开源框架（与 Lua 绑定）。

### 2.14 图形用户界面

- [CEGUI](http://cegui.org.uk/) ： 很灵活的跨平台 GUI 库
- [FLTK](http://www.fltk.org/index.php) ：快速，轻量级的跨平台的 C++GUI 工具包。
- [GTK+](http://www.gtk.org/)： 用于创建图形用户界面的跨平台工具包
- [gtkmm](http://www.gtkmm.org/en/) ：用于受欢迎的 GUI 库 GTK + 的官方 C++ 接口。
- [imgui](https://github.com/ocornut/imgui)：拥有最小依赖关系的立即模式图形用户界面
- [libRocket](http://librocket.com/) ：[libRocket](http://librocket.com/) 是一个 C++ HTML/CSS 游戏接口中间件
- [MyGUI](http://mygui.info/) ：快速，灵活，简单的 GUI
- [Ncurses](http://invisible-island.net/ncurses/)：终端用户界面
- [QCustomPlot](http://qcustomplot.com/) ：没有更多依赖关系的 Qt 绘图控件
- [Qwt](http://qwt.sourceforge.net/) ：用户与技术应用的 Qt 控件
- [QwtPlot3D](http://qwtplot3d.sourceforge.net/) ：功能丰富的基于 Qt/OpenGL 的 C++ 编程库，本质上提供了一群 3D 控件
- [OtterUI](https://github.com/Twolewis/OtterUI) ：[OtterUI](https://github.com/Twolewis/OtterUI) 是用于嵌入式系统和互动娱乐软件的用户界面开发解决方案
- [PDCurses](http://pdcurses.sourceforge.net/) 包含源代码和预编译库的公共图形函数库
- [wxWidgets](http://wxwidgets.org/) C++ 库，允许开发人员使用一个代码库可以为 widows， Mac OS X，Linux 和其他平台创建应用程序

### 2.15 图形

- [bgfx](https://github.com/bkaradzic/bgfx)：跨平台的渲染库
- [Cairo](http://www.cairographics.org/)：支持多种输出设备的 2D 图形库
- [Horde3D](https://github.com/horde3d/Horde3D) 一个小型的 3D 渲染和动画引擎
- [magnum](https://github.com/mosra/magnum) C++11 和 OpenGL 2D/3D 图形引擎
- [Ogre 3D](http://www.ogre3d.org/) 用 C++ 编写的一个面向场景，实时，灵活的 3D 渲染引擎（并非游戏引擎）
- [OpenSceneGraph](http://www.openscenegraph.org/) 具有高性能的开源 3D 图形工具包
- [Panda3D](http://www.panda3d.org/) 用于 3D 渲染和游戏开发的框架，用 Python 和 C++ 编写。
- [Skia](https://github.com/google/skia) 用于绘制文字，图形和图像的完整的 2D 图形库
- [urho3d](https://github.com/urho3d/Urho3D) 跨平台的渲染和游戏引擎。

### 2.16 图像处理

- [Boost.GIL](http://www.boost.org/doc/libs/1_56_0/libs/gil/doc/index.html)：通用图像库
- [CImg](http://cimg.sourceforge.net/) ：用于图像处理的小型开源 C++ 工具包
- [CxImage](http://www.xdp.it/cximage.htm) ：用于加载，保存，显示和转换的图像处理和转换库，可以处理的图片格式包括 BMP, JPEG, GIF, PNG, TIFF, MNG, ICO, PCX, TGA, WMF, WBMP, JBG, J2K。
- [FreeImage](http://freeimage.sourceforge.net/) ：开源库，支持现在多媒体应用所需的通用图片格式和其他格式。
- [GDCM](http://gdcm.sourceforge.net/wiki/index.php/Main_Page)：Grassroots DICOM 库
- [ITK](http://www.itk.org/)：跨平台的开源图像分析系统
- [Magick++](http://www.imagemagick.org/script/api.php)：ImageMagick 程序的 C++ 接口
- [MagickWnd](http://www.imagemagick.org/script/api.php)：ImageMagick 程序的 C++ 接口
- [OpenCV](http://opencv.org/) ： 开源计算机视觉类库
- [tesseract-ocr](https://code.google.com/p/tesseract-ocr/)：OCR 引擎
- [VIGRA](https://github.com/ukoethe/vigra) ：用于图像分析通用 C++ 计算机视觉库
- [VTK](http://www.vtk.org/) ：用于 3D 计算机图形学，图像处理和可视化的开源免费软件系统。

### 2.17 国际化

- [gettext](http://www.gnu.org/software/gettext/) ：GNU `gettext’
- [IBM ICU](http://site.icu-project.org/)：提供 Unicode 和全球化支持的 C、C++ 和 Java 库
- [libiconv](http://www.gnu.org/software/libiconv/) ：用于不同字符编码之间的编码转换库

### 2.18 Jason

- [frozen](https://github.com/cesanta/frozen) ： C/C++ 的 Jason 解析生成器
- [Jansson](https://github.com/akheron/jansson) ：进行编解码和处理 Jason 数据的 C 语言库
- [jbson](https://github.com/chrismanning/jbson) ：C++14 中构建和迭代 BSON data, 和 Json 文档的库
- [JeayeSON](https://github.com/jeaye/jeayeson)：非常健全的 C++ JSON 库，只包含头文件
- [JSON++](https://github.com/hjiang/jsonxx) ： C++ JSON 解析器
- [json-parser](https://github.com/udp/json-parser)：用可移植的 ANSI C 编写的 JSON 解析器，占用内存非常少
- [json11](https://github.com/dropbox/json11) ：一个迷你的 C++11 JSON 库
- [jute](https://github.com/amir-s/jute) ：非常简单的 C++ JSON 解析器
- [ibjson](https://github.com/vincenthz/libjson)：C 语言中的 JSON 解析和打印库，很容易和任何模型集成。
- [libjson](http://sourceforge.net/projects/libjson/)：轻量级的 JSON 库
- [PicoJSON](https://github.com/kazuho/picojson)：C++ 中 JSON 解析序列化，只包含头文件
- [qt-json](https://github.com/gaudecker/qt-json) ：用于 JSON 数据和 QVariant 层次间的相互解析的简单类
- [QJson](https://github.com/flavio/qjson)：将 JSON 数据映射到 QVariant 对象的基于 Qt 的库
- [RapidJSON](https://github.com/miloyip/rapidjson)： 用于 C++ 的快速 JSON 解析生成器，包含 SAX 和 DOM 两种风格的 API
- [YAJL](https://github.com/lloyd/yajl) ：C 语言中快速流 JSON 解析库

### 2.19 日志

- [Boost.Log](http://www.boost.org/doc/libs/1_56_0/libs/log/doc/html/index.html) ：设计非常模块化，并且具有扩展性
- [easyloggingpp](https://github.com/easylogging/easyloggingpp)：C++ 日志库，只包含单一的头文件。
- [Log4cpp](http://log4cpp.sourceforge.net/) ：一系列 C++ 类库，灵活添加日志到文件，系统日志，IDSA 和其他地方。
- [templog](http://www.templog.org/)：轻量级 C++ 库，可以添加日志到你的 C++ 应用程序中

### 2.20 机器学习

- [Caffe](https://github.com/BVLC/caffe) ：快速的神经网络框架
- [CCV](https://github.com/liuliu/ccv) ：以 C 语言为核心的现代计算机视觉库
- [mlpack](http://www.mlpack.org/) ：可扩展的 C++ 机器学习库
- [OpenCV](https://github.com/Itseez/opencv)：开源计算机视觉库
- [Recommender](https://github.com/GHamrouni/Recommender)：使用协同过滤进行产品推荐 / 建议的 C 语言库。
- [SHOGUN](https://github.com/shogun-toolbox/shogun)：Shogun 机器学习工具
- [sofia-ml](https://code.google.com/p/sofia-ml/) ：用于机器学习的快速增量算法套件

### 2.21 数学

- [Armadillo](http://arma.sourceforge.net/) ：高质量的 C++ 线性代数库，速度和易用性做到了很好的平衡。语法和 MatlAB 很相似
- [blaze](https://code.google.com/p/blaze-lib/)：高性能的 C++ 数学库，用于密集和稀疏算法。
- [ceres-solver](http://ceres-solver.org/) ：来自谷歌的 C++ 库，用于建模和解决大型复杂非线性最小平方问题。
- [CGal](http://www.cgal.org/)： 高效，可靠的集合算法集合
- [cml](http://cmldev.net/) ：用于游戏和图形的免费 C++ 数学库
- [Eigen](http://eigen.tuxfamily.org/) ：高级 C++ 模板头文件库，包括线性代数，矩阵，向量操作，数值解决和其他相关的算法。
- [GMTL](http://ggt.sourceforge.net/)：数学图形模板库是一组广泛实现基本图形的工具。
- [GMP](https://gmplib.org/)：用于个高精度计算的 C/C++ 库，处理有符号整数，有理数和浮点数。

### 2.22 多媒体

- [GStreamer](http://gstreamer.freedesktop.org/) ：构建媒体处理组件图形的库
- [LIVE555 Streaming Media](http://www.live555.com/liveMedia/) ：使用开放标准协议 (RTP/RTCP, RTSP, SIP) 的多媒体流库
- [libVLC](https://wiki.videolan.org/LibVLC) ：libVLC (VLC SDK) 媒体框架
- [QtAv](https://github.com/wang-bin/QtAV)：基于 Qt 和 FFmpeg 的多媒体播放框架，能够帮助你轻而易举地编写出一个播放器
- [SDL](http://www.libsdl.org/) ：简单直控媒体层
- [SFML](http://www.sfml-dev.org/) ：快速，简单的多媒体库

### 2.23 网络

- [ACE](http://www.cs.wustl.edu/~schmidt/ACE.html)：C++ 面向对象网络变成工具包
- [Boost.Asio](http://think-async.com/)：用于网络和底层 I/O 编程的跨平台的 C++ 库
- [Casablanca](http://casablanca.codeplex.com/)：C++ REST SDK
- [cpp-netlib](http://cpp-netlib.org/)：高级网络编程的开源库集合
- [Dyad.c](https://github.com/rxi/dyad)：C 语言的异步网络
- [libcurl](http://curl.haxx.se/libcurl/) : 多协议文件传输库
- [Mongoose](https://github.com/cesanta/mongoose)：非常轻量级的网络服务器
- [Muduo](https://github.com/chenshuo/muduo) ：用于 Linux 多线程服务器的 C++ 非阻塞网络库
- [net_skeleton](https://github.com/cesanta/net_skeleton) ：C/C++ 的 TCP 客户端 / 服务器库
- [nope.c](https://github.com/riolet/nope.c) ：基于 C 语言的超轻型软件平台，用于可扩展的服务器端和网络应用。 对于 C 编程人员，可以考虑 node.js
- [Onion](https://github.com/davidmoreno/onion) :C 语言 HTTP 服务器库，其设计为轻量级，易使用。
- [POCO](https://github.com/pocoproject)：用于构建网络和基于互联网应用程序的 C++ 类库，可以运行在桌面，服务器，移动和嵌入式系统。
- [RakNet](https://github.com/OculusVR/RakNet)：为游戏开发人员提供的跨平台的开源 C++ 网络引擎。
- [Tuf o](https://github.com/vinipsmaker/tufao) ：用于 Qt 之上的 C++ 构建的异步 Web 框架。
- [WebSocket++](https://github.com/zaphoyd/websocketpp) ：基于 C++/Boost Aiso 的 websocket 客户端 / 服务器库
- [ZeroMQ](http://zeromq.org/) ：高速，模块化的异步通信库

### 2.24 物理学

动力学仿真引擎

- [Box2D](https://code.google.com/p/box2d/)：2D 的游戏物理引擎。
- [Bullet](https://github.com/bulletphysics/bullet3) ：3D 的游戏物理引擎。
- [Chipmunk](https://github.com/slembcke/Chipmunk2D) ：快速，轻量级的 2D 游戏物理库
- [LiquidFun](https://github.com/google/liquidfun)：2D 的游戏物理引擎
- [ODE](http://www.ode.org/) ：开放动力学引擎 - 开源，高性能库，模拟刚体动力学。
- [ofxBox2d](https://github.com/vanderlin/ofxBox2d)：Box2D 开源框架包装器。
- [Simbody](https://github.com/simbody/simbody) ：高性能 C++ 多体动力学 / 物理库，模拟关节生物力学和机械系统，像车辆，机器人和人体骨骼。

### 2.25 机器人学

- [MOOS-IvP](http://moos-ivp.org/) ：一组开源 C++ 模块，提供机器人平台的自主权，尤其是自主的海洋车辆。
- [MRPT](http://www.mrpt.org/)：移动机器人编程工具包
- [PCL](https://github.com/PointCloudLibrary/pcl) ：点云库是一个独立的，大规模的开放项目，用于 2D/3D 图像和点云处理。
- [Robotics Library (RL)](http://www.roboticslibrary.org/)： 一个独立的 C++ 库，包括机器人动力学，运动规划和控制。
- [RobWork](http://www.robwork.dk/jrobwork/)：一组 C++ 库的集合，用于机器人系统的仿真和控制。
- [ROS](http://wiki.ros.org/) ：机器人操作系统，提供了一些库和工具帮助软件开发人员创建机器人应用程序。

### 2.26 科学计算

- [FFTW](http://www.fftw.org/) : 用一维或者多维计算 DFT 的 C 语言库。
- [GSL](http://www.gnu.org/software/gsl/)：GNU 科学库。

### 2.27 脚本

- [ChaiScript](https://github.com/ChaiScript/ChaiScript/) ：用于 C++ 的易于使用的嵌入式脚本语言。
- [Lua](http://www.lua.org/) ：用于配置文件和基本应用程序脚本的小型快速脚本引擎。
- [luacxx](https://github.com/dafrito/luacxx)：用于创建 Lua 绑定的 C++ 11 API
- [SWIG](http://www.swig.org/) ：一个可以让你的 C++ 代码链接到 JavaScript，Perl，PHP，Python，Tcl 和 Ruby 的包装器 / 接口生成器
- [V7](https://github.com/cesanta/v7)：嵌入式的 JavaScript 引擎。
- [V8](http://code.google.com/p/v8/) ：谷歌的快速 JavaScript 引擎，可以被嵌入到任何 C++ 应用程序中。

### 2.28 序列化

- [Cap’n Proto](http://kentonv.github.io/capnproto/) ：快速数据交换格式和 RPC 系统。
- [cereal](https://github.com/USCiLab/cereal) ：C++11 序列化库
- [FlatBuffers](https://github.com/google/flatbuffers) ：内存高效的序列化库
- [MessagePack](https://github.com/msgpack/msgpack-c) ：C/C++ 的高效二进制序列化库，例如 JSON
- [protobuf](http://code.google.com/p/protobuf/) ：协议缓冲，谷歌的数据交换格式。
- [protobuf-c](https://github.com/protobuf-c/protobuf-c) ：C 语言的协议缓冲实现
- [SimpleBinaryEncoding](https://github.com/real-logic/simple-binary-encoding)：用于低延迟应用程序的对二进制格式的应用程序信息的编码和解码。
- [Thrift](https://thrift.apache.org/) ：高效的跨语言 IPC/RPC，用于 C++，Java，Python，PHP，C# 和其它多种语言中，最初由 Twitter 开发。

### 2.29 视频

- [libvpx](http://www.webmproject.org/code/) ：VP8/VP9 编码解码 SDK
- [FFmpeg](https://www.ffmpeg.org/) ：一个完整的，跨平台的解决方案，用于记录，转换视频和音频流。
- [libde265](https://github.com/strukturag/libde265) ：开放的 h.265 视频编解码器的实现。
- [OpenH264](https://github.com/cisco/openh264)：开源 H.364 编解码器。
- [Theora](http://www.theora.org/) ：免费开源的视频压缩格式。

### 2.30 虚拟机

- [CarpVM](https://github.com/tekknolagi/carp)：C 中有趣的 VM，让我们一起来看看这个。
- [MicroPython](https://github.com/micropython/micropython) ：旨在实现单片机上 Python3.x 的实现
- [TinyVM](https://github.com/jakogut/tinyvm)：用纯粹的 ANSI C 编写的小型，快速，轻量级的虚拟机。

### 2.31 Web 应用框架

- [Civetweb](https://github.com/bel2125/civetweb) ：提供易于使用，强大的，C/C++ 嵌入式 Web 服务器，带有可选的 CGI，SSL 和 Lua 支持。
- [CppCMS](http://cppcms.com/) ：免费高性能的 Web 开发框架（不是 CMS）.
- [Crow](https://github.com/ipkn/crow) ：一个 C++ 微型 web 框架（灵感来自于 Python Flask）
- [Kore](https://kore.io/) : 使用 C 语言开发的用于 web 应用程序的超快速和灵活的 web 服务器 / 框架。
- [libOnion](http://www.coralbits.com/libonion/)：轻量级的库，帮助你使用 C 编程语言创建 web 服务器。
- [QDjango](https://github.com/jlaine/qdjango/)：使用 C++ 编写的，基于 Qt 库的 web 框架，试图效仿 Django API，因此得此名。
- [Wt](http://www.webtoolkit.eu/wt) ：开发 Web 应用的 C++ 库。

### 2.32 XML

XML 就是个垃圾，xml 的解析很烦人，对于计算机它也是个灾难。这种糟糕的东西完全没有存在的理由了。-Linus Torvalds

- [Expat](http://www.libexpat.org/) ：用 C 语言编写的 xml 解析库
- [Libxml2](http://xmlsoft.org/) ：Gnome 的 xml C 解析器和工具包
- [libxml++](http://libxmlplusplus.sourceforge.net/) ：C++ 的 xml 解析器
- [PugiXML](http://pugixml.org/) ：用于 C++ 的，支持 XPath 的轻量级，简单快速的 XML 解析器。
- [RapidXml](http://rapidxml.sourceforge.net/) ：试图创建最快速的 XML 解析器，同时保持易用性，可移植性和合理的 W3C 兼容性。
- [TinyXML](http://sourceforge.net/projects/tinyxml/) ：简单小型的 C++XML 解析器，可以很容易地集成到其它项目中。
- [TinyXML2](https://github.com/leethomason/tinyxml2)：简单快速的 C++CML 解析器，可以很容易集成到其它项目中。
- [TinyXML++](https://code.google.com/p/ticpp/)：TinyXML 的一个全新的接口，使用了 C++ 的许多许多优势，模板，异常和更好的异常处理。
- [Xerces-C++](http://xerces.apache.org/xerces-c/) ：用可移植的 C++ 的子集编写的 XML 验证解析器。

### 2.33 多项混杂

一些有用的库或者工具，但是不适合上面的分类，或者还没有分类。

- [C++ Format](https://github.com/cppformat/cppformat) ：C++ 的小型，安全和快速格式化库
- [casacore](https://code.google.com/p/casacore/) ：从 aips++ 派生的一系列 C++ 核心库
- [cxx-prettyprint](https://github.com/louisdx/cxx-prettyprint)：用于 C++ 容器的打印库
- [DynaPDF](http://www.dynaforms.com/) ：易于使用的 PDF 生成库
- [gcc-poison](https://github.com/leafsr/gcc-poison) ：帮助开发人员禁止应用程序中的不安全的 C/C++ 函数的简单的头文件。
- [googlemock](http://code.google.com/p/googlemock/)：编写和使用 C++ 模拟类的库
- [HTTP Parser](https://github.com/joyent/http-parser) ：C 的 http 请求 / 响应解析器
- [libcpuid](https://github.com/anrieff/libcpuid) ：用于 x86 CPU 检测盒特征提取的小型 C 库
- [libevil](https://github.com/avati/libevil) ：许可证管理器
- [libusb](http://www.libusb.org/)：允许移动访问 USB 设备的通用 USB 库
- [PCRE](http://pcre.org/)：正则表达式 C 库，灵感来自于 Perl 中正则表达式的功能。
- [Remote Call Framework](http://www.deltavsoft.com/) ：C++ 的进程间通信框架。
- [Scintilla](http://scintilla.org/) ：开源的代码编辑控件
- [Serial Communication Library](https://github.com/wjwwood/serial) ：C++ 语言编写的跨平台，串口库。
- [SDS](https://github.com/antirez/sds)：C 的简单动态字符串库
- [SLDR](https://github.com/cesanta/sldr) ：超轻的 DNS 解析器
- [SLRE](https://github.com/cesanta/slre)： 超轻的正则表达式库
- [Stage](https://github.com/rtv/Stage) ：移动机器人模拟器
- [VarTypes](https://code.google.com/p/vartypes/)：C++/Qt4 功能丰富，面向对象的管理变量的框架。
- [ZBar](http://zbar.sourceforge.net/)：‘条形码扫描器’库，可以扫描照片，图片和视频流中的条形码，并返回结果。
- [CppVerbalExpressions](https://github.com/VerbalExpressions/CppVerbalExpressions) ：易于使用的 C++ 正则表达式
- [QtVerbalExpressions](https://github.com/VerbalExpressions/QtVerbalExpressions)：基于 C++ VerbalExpressions 库的 Qt 库
- [PHP-CPP](https://github.com/CopernicaMarketingSoftware/PHP-CPP)：使用 C++ 来构建 PHP 扩展的库
- [Better String](http://bstring.sourceforge.net/) ：C 的另一个字符串库，功能更丰富，但是没有缓冲溢出问题，还包含了一个 C++ 包装器。

### 2.34 软件

用于创建开发环境的软件

### 2.35 编译器

C/C++ 编译器列表

- [Clang](http://clang.llvm.org/) : 由苹果公司开发的
- [GCC](https://gcc.gnu.org/)：GNU 编译器集合
- [Intel C++ Compiler](https://software.intel.com/en-us/c-compilers) ：由英特尔公司开发
- [LLVM](http://llvm.org/) ：模块化和可重用编译器和工具链技术的集合
- [Microsoft Visual C++](http://msdn.microsoft.com/en-us/vstudio/hh386302.aspx) ：MSVC，由微软公司开发
- [Open WatCom](http://www.openwatcom.org/index.php/Main_Page) ：Watcom，C，C++ 和 Fortran 交叉编译器和工具
- [TCC](http://bellard.org/tcc/) ：轻量级的 C 语言编译器

### 2.36 在线编译器

在线 C/C++ 编译器列表

- [codepad](http://codepad.org/) ：在线编译器 / 解释器，一个简单的协作工具
- [CodeTwist](http://codetwist.com/)：一个简单的在线编译器 / 解释器，你可以粘贴的 C,C++ 或者 Java 代码，在线执行并查看结果
- [coliru](http://coliru.stacked-crooked.com/) ：在线编译器 /shell， 支持各种 C++ 编译器
- [Compiler Explorer](http://gcc.godbolt.org/)：交互式编译器，可以进行汇编输出
- [CompileOnline](http://www.compileonline.com/compile_cpp11_online.php)：Linux 上在线编译和执行 C++ 程序
- [Ideone](http://ideone.com/) ：一个在线编译器和调试工具，允许你在线编译源代码并执行，支持 60 多种编程语言。

### 2.37 调试器

C/C++ 调试器列表

- [Comparison of debuggers](http://en.wikipedia.org/wiki/Comparison_of_debuggers) ：来自维基百科的调试器列表
- [GDB](https://www.gnu.org/software/gdb) ：GNU 调试器
- [Valgrind](http://valgrind.org/)：内存调试，内存泄露检测，性能分析工具。

### 2.38 集成开发环境（IDE）

C/C++ 集成开发环境列表

- [AppCode](http://www.jetbrains.com/objc/) ：构建与 JetBrains’ IntelliJ IDEA 平台上的用于 Objective-C，C,C++，Java 和 Java 开发的集成开发环境
- [CLion](http://www.jetbrains.com/clion/)：来自 JetBrains 的跨平台的 C/C++ 的集成开发环境
- [Code::Blocks](http://www.codeblocks.org/) ：免费 C，C++ 和 Fortran 的集成开发环境
- [CodeLite](http://codelite.org/) ：另一个跨平台的免费的 C/C++ 集成开发环境
- [Dev-C++](http://sourceforge.net/projects/orwelldevcpp/)：可移植的 C/C++/C++11 集成开发环境
- [Eclipse CDT](http://www.eclipse.org/cdt/)：基于 Eclipse 平台的功能齐全的 C 和 C++ 集成开发环境
- [Geany](http://www.geany.org/) ：轻量级的快速，跨平台的集成开发环境。
- [IBM VisualAge](http://www-03.ibm.com/software/products/en/visgen) ：来自 IBM 的家庭计算机集成开发环境。
- [Irony-mode](https://github.com/Sarcasm/irony-mode)：由 libclang 驱动的用于 Emacs 的 C/C++ 微模式
- [KDevelop](https://www.kdevelop.org/)：免费开源集成开发环境
- [Microsoft Visual Studio](http://www.visualstudio.com/) ：来自微软的集成开发环境
- [NetBeans](https://netbeans.org/) ：主要用于 Java 开发的的集成开发环境，也支持其他语言，尤其是 PHP，C/C++ 和 HTML5。
- [Qt Creator](http://qt-project.org/)：跨平台的 C++，Javascript 和 QML 集成开发环境，也是 Qt SDK 的一部分。
- [rtags](https://github.com/Andersbakken/rtags)：C/C++ 的客户端服务器索引，用于 跟基于 clang 的 emacs 的集成
- [Xcode](https://developer.apple.com/xcode/) ：由苹果公司开发
- [YouCompleteMe](https://valloric.github.io/YouCompleteMe/)：一个用于 Vim 的根据你敲的代码快速模糊搜索并进行代码补全的引擎。

### 2.39 构建系统

- [Bear](https://github.com/rizsotto/Bear) ：用于为 clang 工具生成编译数据库的工具
- [Biicode](https://www.biicode.com/)：基于文件的简单依赖管理器。
- [CMake](http://www.cmake.org/) ：跨平台的免费开源软件用于管理软件使用独立编译的方法进行构建的过程。
- [CPM](https://github.com/iauns/cpm)：基于 CMake 和 Git 的 C++ 包管理器
- [FASTBuild](http://www.fastbuild.org/docs/home.html)：高性能，开源的构建系统，支持高度可扩展性的编译，缓冲和网络分布。
- [Ninja](http://martine.github.io/ninja/) ：专注于速度的小型构建系统
- [Scons](http://www.scons.org/) ：使用 Python scipt 配置的软件构建工具
- [tundra](https://github.com/deplinenoise/tundra) ：高性能的代码构建系统，甚至对于非常大型的软件项目，也能提供最好的增量构建次数。
- [tup](http://gittup.org/tup/)：基于文件的构建系统，用于后台监控变化的文件。

### 2.40 静态代码分析

提高质量，减少瑕疵的代码分析工具列表

- [Cppcheck](http://cppcheck.sourceforge.net/) ：静态 C/C++ 代码分析工具
- [include-what-you-use](https://code.google.com/p/include-what-you-use/) ：使用 clang 进行代码分析的工具，可以 #include 在 C 和 C++ 文件中。
- [OCLint](http://oclint.org/) ：用于 C，C++ 和 Objective-C 的静态源代码分析工具，用于提高质量，减少瑕疵。
- [Clang Static Analyzer](http://clang-analyzer.llvm.org/index.html)：查找 C，C++ 和 Objective-C 程序 bug 的源代码分析工具
- [List of tools for static code analysis](http://en.wikipedia.org/wiki/List_of_tools_for_static_code_analysis#C.2FC.2B.2B) ：来自维基百科的静态代码分析工具列表



感谢平凡之路和 fffaraz 的整理，转载请注明出处。
