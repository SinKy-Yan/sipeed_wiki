---
title: MaixCAM-Pro -- 快速落地 AI 视觉、听觉应用
---

<div style="width:100%; display:flex;justify-content: center;">

![maixcam-pro](/static/image/maixcam_pro.png)

</div>

<div style="padding: 1em 0 0 0; display: flex; justify-content: center">
    <a target="_blank" style="margin: 1em;color: white; font-size: 0.9em; border-radius: 0.3em; padding: 0.5em 2em; background-color: #a80202" href="https://item.taobao.com/item.htm?id=846226367137">淘宝</a>
    <a target="_blank" style="margin: 1em;color: white; font-size: 0.9em; border-radius: 0.3em; padding: 0.5em 2em; background-color: #a80202" href="https://www.aliexpress.com/store/911876460">速卖通</a>
</div>


## MaixCAM-Pro 简介

MaixCAM 是为更好地落地 AI 视觉、听觉和 AIOT 应用而设计的一款硬件产品，一个能快速验证产品原型且能快速量产的平台。
提供了强大且高性价比的处理器，配套的摄像头、屏幕、WiFi 等，以及完善和非常易用的软件生态。

<div style="display: flex; justify-content: left">
    <a target="_blank" style="margin: 1em;color: white; font-size: 0.9em; border-radius: 0.3em; padding: 0.5em 2em; background-color: #a80202" href="https://wiki.sipeed.com/maixpy/">更多功能介绍请看 MaixPy 主页</a>
</div>

**应用场景和人群**：
* **AI算法落地**： AI 算法工程师可以快速将自己的 AI 模型部署到实体硬件（MaixCAM)上，提供易用的模型转换工具和 SDK。
* **STEM 教育**： 提供易用的 MaixPy SDK 和配套开发工具，以及在线模型训练平台，老师无需软硬件开发，专注教学，学生可以快速上手。
* **高校科研和教育**： 提供丰富的文档和教程，高校学生各个阶段的学生都有合适的学习路线，RISC-V 和 AI 前沿技术也是科研的好帮手。
* **创客和工程师的原型开发利器**：精心设计的硬件，丰富的外设，超易用的软件，让你的有趣想法和产品快速落地，不用身陷基础软硬件开发的泥潭。
* **企业产品升级、落地**：无需昂贵的研发成本快速落地产品，或者用于辅助产品比如产线 QA，旧设备使用 AI 视觉实现智能化等。
* **竞赛好帮手**：MaixCAM + MaixPy + MaixCDK 可以快速实现很多创新和功能，适合作为比赛指定软硬件平台，选手也可以依靠生态的开发效率赢得比赛， Maix 系列产品和 MaixPy 已经被用在各种比赛中获得奖项。


## MaixCAM-Pro 硬件简介

> MaixCAM-Pro 相比 [MaixCAM](./README.md) 重新设计了 PCB 和外壳以及有部分外设升级， 加粗为和 MaixCAM 的不同处

| 组件 | 描述 |
| --- | --- |
| CPU 大核 | 1GHz RISC-V C906 处理器（另外还有一个 1GHz ARM A53 核心可二选一使用），跑 Linux |
| CPU 小核 | 700MHz RISC-V C906， 跑 RTOS |
| CPU 低功耗核 | 25~300MHz 8051 处理器，用于低功耗应用 |
| NPU | 1TOPS@INT8， 支持 BF16 模型，算子支持丰富，支持常见模型比如 Mobilenetv2, YOLOv5, YOLOv8等 |
| 内存 | 256MB DDR3 |
| 存储 | TF 卡启动 / SD NAND 启动 |
| 摄像头 | 最高支持 5M 摄像头，官方支持 4M GC4653 和 OS04A10 摄像头（4 lane MIPI CSI 输入，22Pin 接口，支持拆分双路 CSI） |
| 屏幕 | **2.4 寸高清 IPS 电容触摸屏， 分辨率 640x480**（2 lane MIPI DSI 输出，标准 31pin 接口，6pin 电容触摸屏） |
| 音频输出 | 板载PA功放 + **1W 喇叭** |
| 音频输入 | 板载模拟硅麦，可直接收音 |
| 网络 | 板载 WiFi6 + BLE5.4 模组，可定制 以太网版本 |
| USB | Type-C USB2.0，支持Device和Host模式，支持 USB 摄像头 |
| IO 接口 | **2.54mm PMOD 接口， 引出 12 个 IO + Vsys/3.3v/GND 接口 + 1.25mm 5pin扩展接口**|
| 按键 | 1 x RST 按键 + 1 x USER（功能） 按键 + **1 x 电源按钮**|
| LED | 电源指示灯 + 用户 LED + **照明 LED** |
| 编解码 | H.264 / H.265 / MJPEG 硬解码， 支持 2k@30fps 编解码 |
| 外设 | I2C/SPI/UART/ADC/PWM/WDT 等常见外设 |
| 电源 | **独立电源管理芯片AXP2101，支持锂电池充放电管理，并且提供带锂电池版本** |
| 外壳 | **3D 打印+亚克力外壳， 1/4 英寸标准螺纹固定孔** |
| IMU | **板载六轴 IMU 传感器（三轴加速度+三轴角速度）** |
| RTC | **板载 BM8653 RTC 芯片+纽扣电池，断电时间仍然正确** |
| 尺寸 | **无电池版本外壳 67x51x12mm, 带电池版本厚度 16mm**  |


## MaixCAM 软件生态

我们不只是做了硬件，更为 MaixCAM 提供了一套完整的软件生态，包括：

| 名称 | 描述 | 图片/视频 |
| --- | --- | --- |
| **[MaixPy](https://wiki.sipeed.com/maixpy/)** | Python 开发包， 提供丰富且使用简单的 API，针对 MaixCAM 进行优化，支持硬件加速，提供丰富文档教程 | 请看[MaixPy 主页](https://wiki.sipeed.com/maixpy/) |
| [MaixVision](https://wiki.sipeed.com/maixvision) | AI 视觉 IDE，编程、代码运行、图像实时预览，甚至图形化编程等等，大大降低开发环境搭建难度和使用门槛 | ![MaixVision](../../assets/maixcam/maixvision.jpg)  <video playsinline controls muted preload style="width:100%" src="https://wiki.sipeed.com/maixpy/static/video/maixvision.mp4"></video> |
| [MaixHub](https://maixhub.com) | 在线 AI 模型训练平台，无需 AI 知识和昂贵的训练设备，一键训练模型，一键部署到 MaixCAM | ![MaixVision](../../assets/maixcam/maixhub.jpg) |
| [MaixCDK](https://github.com/sipeed/MaixCDK) | MaixPy 的 C++版本，熟悉 C/C++ 的开发者立刻上手 | 请看[MaixCDK 主页](https://github.com/sipeed/MaixCDK) |
| [应用商城](https://maixhub.com/app) | 提供各种应用和工具，无需开发直接下载使用，开发者也可以上传分享应用 | 请看 [MaixHub 应用商城](https://maixhub.com/app) |
| [分享广场](https://maixhub.com/share) | 开发者分享经验和项目 | 请看 [MaixHub 分像广场](https://maixhub.com/share) |


## 资料汇总

### MaixCAM 专属资料（Sipeed 提供）

* [MaixCAM-Pro 官方文档](https://wiki.sipeed.com/maixcam-pro)（本文档）
* [MaixPy 官方文档](https://wiki.sipeed.com/maixpy/)（Python SDK）（[MaixPy 源码](https://github.com/sipeed/MaixPy)）
* [MaixCDK](https://github.com/sipeed/MaixCDK)（C/C++ SDK）（[MaixCDK 源码](https://github.com/sipeed/MaixCDK)）
* [系统源码](https://github.com/sipeed/LicheeRV-Nano-Build)
* [硬件相关资料](https://dl.sipeed.com/shareURL/MaixCAM/MaixCAM_Pro)
* 外壳和支架：可以在[外壳文档](./assemble.md) 看到介绍，另外还开源了 外壳、支架等 3D 模型文件，请到[makerworld.com](https://makerworld.com/)（推荐） 或[makerworld.com.cn](https://makerworld.com.cn) 搜索 `MaixCAM`。
* 接口图：
![maixcam_pro_io](../../assets/maixcam/maixcam_pro_io.png)


### 芯片资料

MaixCAM-Pro 其基于算能的SG2002 芯片，所以也可以参考它们的资料，也可以参考 Sipeed 的 LiecheeRV-Nano 核心板文档。
>! 注意：MaixCAM-Pro 可以使用 LicheeRV-Nano 和 SG2002 的资料， 反之 **LicheeRV-Nano 和其它 SG2002 芯片产品没法使用 MaixPy MaixCDK MaixVision 等软件**，请不要购买错误浪费时间和金钱。
> 如果你希望快速上手开发应用，请选择 MaixCAM, 如果你是资深 Linux 开发者，只想基于 SG2002 原厂资料开发，可以选择 LicheeRV-Nano。

* [Datasheet](https://github.com/sophgo/sophgo-doc/releases) （寄存器级别的资料）
* [LicheeRV-Nano 开发板资料](https://wiki.sipeed.com/hardware/zh/lichee/RV_Nano/1_intro.html)
* [工具链下载](https://sophon-file.sophon.cn/sophon-prod-s3/drive/23/03/07/16/host-tools.tar.gz)
* [算能 SDK 开发文档汇总](https://developer.sophgo.com/thread/471.html)
* [算能 HDK 开发文档汇总](https://developer.sophgo.com/thread/472.html)
* [算能 TPU 开发文档汇总](https://developer.sophgo.com/thread/473.html)
* [算能 TDL 开发文档汇总](https://developer.sophgo.com/thread/556.html)（基于 TPU 的高层API 封装）

### 社区资料

* [MaixHub 应用商城](https://maixhub.com/app)
* [MaixHub 分享广场](https://maixhub.com/share)
* [makerworld.com](https://makerworld.com/)(推荐) 或者 [makerworld.com.cn](https://makerworld.com.cn) 搜索 `MaixCAM`
* [Bilibili](https://bilibili.com) 搜索 `MaixCAM` 或者 `MaixPy`

## 购买

* [Sipeed 淘宝](https://sipeed.taobao.com/)
* [AliExpress](https://www.aliexpress.com/store/911876460)


