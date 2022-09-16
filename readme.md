# 黑苹果指南

转载请注明出处，可以二创。

如果你在安装时遇到问题，可在飞机号：t.me/Mistry_Rain

所有的操作均来自互联网，遇到问题请你自己负责！

问问题请做一个有素质的人！

# 前言

## 这是一篇适合对黑苹果毫无了解的小白

    适用于：你已经买到电脑，想装黑苹果

若你准备买一台可以装黑苹果设备

参考 [笔记本](https://github.com/daliansky/Hackintosh) [台式机](https://macx.top/18202.html)

## 在开始前，你至少需要确保：

    会进bios 
    
    会至少一点点英语
    
    有手、耐心
    
    此文章用的是传统安装法，需要一个U盘

## 文章会用到的简写

1.搜索**XXX+中文(括号内是英文，在谷歌搜)**

2.笔记本和电脑统称电脑，如有特殊说明（笔记本有电池、触控板啥的），请按照特殊说明的来办

3.已经默认你会搭梯子、会使用GitHub(不接受此类问题)

# Step1:思考

    ·想想你装黑苹果来干嘛？
    
    ·愿不愿意一遍一遍的重启排错？
    
    ·愿不愿意仔仔细细的阅读一些英文的？甚至读不懂的俄语？
    
    ·能不能接受不稳定？
    
    ·需要大量时间，大量精力？

# Step2:明确自己的配置

## Why?

 ~~黑果的大概启动原理是：修改config和DSDT来启动OS X~~

    当然这么说，显然不适合小白。

对于小白来说，你需要做的就是去搜一下 **机型+EFI** 即可

## 有现成的EFI

国内买的就去国内平台（包括但不限于bilibili、百度、各种论坛）国外买的去Google搜型号+Hackintosh

你的电脑如果找不到或者太冷门，且也想装黑苹果。就需要自己配EFI

## 无

如果没有，就要按照下面的内容来自行配置EFI

使用 **鲁大师、aida64、百度搜** 等，一定要准确的知道自己的配置，例如图一

# Step3 :配置EFI

    这是一个 ！大点！
    请结合多方信息，
    不要只看我的这篇、也不要局限于国内互联网。

## 你至少需要知道

    1.黑苹果不怎么挑U，但太老、太偏、AMD，就节约时间不考虑了。上网本（奔腾、赛扬就直接pass不得行）
    
    2.Intel的集显(HD+一些数字)、AMD的独立显卡大多都可驱动，这个请搜索 “显卡型号+黑苹果”
    
    3.网卡能驱动上的很少，能驱动的也有各种特殊方法。
    具体情况请自行搜索，本文不展开
    
    4.声卡同理，请自行搜索

## 下载工作

### 必须下载（无论你是什么电脑，当然苹果电脑除外）

这里的文件[参考](https://dortania.github.io/OpenCore-Install-Guide/ktext.html#must-haves)部分软件请记住他的别称（打在括号里的）

    请将你下载好的文件放在一起，软件请安装。请确保所有的东西你都能找到！

1.编辑plist配置的[plist编辑器](https://github.com/corpnewt/ProperTree) 或者[OpenCoreCFG](https://mackie100projects.altervista.org/opencore-configurator/) 

2.必备，下载release[最简EFI](https://github.com/acidanthera/OpenCorePkg/releases)

3.[支持文件](https://github.com/acidanthera/AppleSupportPkg/releases)

4.diskgeunis(区分工具)百度去下

5.[Lilu](https://github.com/acidanthera/Lilu/releases)

6.[VirtualSMC](https://github.com/acidanthera/VirtualSMC/releases)

7.[WhateverGreen !部分AMD的集显不能装！](https://github.com/acidanthera/WhateverGreen/releases)

### 这里是笔记本的附加部分，台式机请跳过

    因为有电池、键盘鼠标等，笔记本用户大多都需要补充这些驱动。
    当然凡事无绝对，你无法确保有些吃饱没事干，搞特殊，
    这一部分适用于大部分用户，如果这一部分按照广普的教程不行，请百度搜索

#### 所有笔记本用户

1.SMCProcessor.kext

2.SMCSuperIO.kext

3.SMCLightSensor.kext

4.SMCBatteryManager.kext

5.SMCDellSensors.kext(仅限dell用户)

##### AMD用户需要额外补充的驱动

1.[AMDProcesser](https://github.com/trulyspinach/SMCAMDProcessor)

2.[AMDRadeonGPU](https://github.com/aluveitie/RadeonSensor)

## 正式开始

    个人建议你那个小本本记录下

### 显卡

#### Intel核显 （也就是整个电脑没有显卡）

直接用这个[工具](https://www.123pan.com/s/rd39-MkpOd)特别省事

#### Nvdia  ~~仅支持到10.13.6~~
[参考](https://www.bilibili.com/video/BV1wr4y1r78X?spm_id_from=333.337.search-card.all.click&vd_source=b2ed1387674e77df3a3f4f6acfe5a846)
这个部分争议较大，且这个技术比较新，又加上我没有Nvdia的显卡无法测试

所以英伟达用户请自行测试
#### AMD显卡（独显，如果你是vega8这类集显，要么等，要么C++逆向）

    AMD显卡要么就是免驱，要么就是仿冒ID这一步AMD用户可以大喊一声：AMD YES
    如果你是vega8的用户，且你刚好会C++，接触过逆向工程。欢迎联系我
 
 ### 声卡
 ### 网卡


