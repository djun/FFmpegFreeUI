[《如何在 GitHub 下载软件》小白提醒：你的需求是下载这个软件去使用而不是要工程文件，点此去 Releases 下载发行版才是下载软件；上面的 Code 是下载源代码；我都写成这样了如果你在 Releases 里又下成了源代码，那真的是人机，都是手机和短视频害的。](https://github.com/Lake1059/FFmpegFreeUI/releases) 本文已包含新手内容，就看有没有心思学了。

## FFmpegFreeUI

FFmpegFreeUI（简称 3FUI）是在 Windows 上的 [FFmpeg](https://ffmpeg.org) 的专业交互外壳，使用 .NET 10 框架，使用纯 WinForm 开发，配合 SunnyUI 和自绘制打造专业高效的暗黑风格界面。3FUI 是一个完全倒贴开发的项目，除了用户自愿赞助以外没有任何收入来源。如果我的设计对你有帮助，请帮助我宣传或者考虑资金支持。另外，我不会接受任何广告植入合作！

设计定位：3FUI 的目标是做一款轻度专业参数调整的转码软件，并非行业深度专业软件；让普通人能够通过图形化界面接触到较为全面的通用参数来轻松压制和转换格式。

> 广告词：难以忍受格式工厂的烦人捆绑？行业专业软件限制太多？小作坊产品过于业余？来用 3FUI 就对了，专注转码，不干别的，真免费，真自由，真专业，真开源！

[Wine](https://www.winehq.org) 是一个在多种 POSIX-compliant 操作系统上运行 Windows 应用的兼容层，如果能够在 macOS 和 Linux 上安装并正确使用，理论上可以直接在这些操作系统上使用 3FUI。3FUI 内部的一些逻辑已经针对跨平台进行兼容（路径拼接和启动 process 已移除后缀）。请自行尝试可行性，不要来问我这部分的内容，因为我买不起苹果电脑，也用不来 Linux。

| 统计项目             | 即时结果                                                     |
| -------------------- | ------------------------------------------------------------ |
| 总下载量             | ![](https://img.shields.io/github/downloads/Lake1059/FFmpegFreeUI/total) |
| x64 单文件下载量     | ![](https://img.shields.io/github/downloads/Lake1059/FFmpegFreeUI/FFmpegFreeUI.x64.exe) |
| x64 松散文件下载量   | ![](https://img.shields.io/github/downloads/Lake1059/FFmpegFreeUI/FFmpegFreeUI.x64.SelfContained.zip) |
| x86 单文件下载量     | ![](https://img.shields.io/github/downloads/Lake1059/FFmpegFreeUI/FFmpegFreeUI.x86.exe) |
| x86 松散文件下载量   | ![](https://img.shields.io/github/downloads/Lake1059/FFmpegFreeUI/FFmpegFreeUI.x86.SelfContained.zip) |
| arm64 单文件下载量   | ![](https://img.shields.io/github/downloads/Lake1059/FFmpegFreeUI/FFmpegFreeUI.arm64.exe) |
| arm64 松散文件下载量 | ![](https://img.shields.io/github/downloads/Lake1059/FFmpegFreeUI/FFmpegFreeUI.arm64.SelfContained.zip) |

> **为什么提供松散文件版本？**
> 单文件版本是纯二进制文件，对系统要求严苛，一些电脑即便正确下载了对应架构也无法运行，而松散文件版本通过中间型解释代码来运行，更好地适应各种系统环境。

> **为什么不提供需要安装运行库的最小体积版本？**
> .NET 10 还是太超前了，目前还是预览版，更不要提很多人的 Windows 都是被暗中魔改过的，在之前的项目经验中大量的电脑死活无法安装成功，或是装上了也没用。

> **长时间使用的崩溃问题解决了吗？**
> 已经在内部测试版本 **0.7 EA 4** 中彻底解决，可直接加群提前获取

### 为什么选择 3FUI

- **底层逻辑基于预设**<br>保存到 json 文件中，由用户自行管理，以及与他人分享<br>注意：不保证跨版本的兼容，因为参数项目和数据类型可能更改

- **专业参数，而非业余表述**<br>低中高是什么玩意，真实参数才是真理<br>且大多数地方直接标出参数名称，更易于上手

- **准确显示 ffmpeg 输出的信息**<br>更易于尝试新方案

- **实时计算剩余时间**<br>

  你的时间非常值钱
  
- **预估最终输出大小**<br>

  当然这肯定是不准的，但有个大概总比没有强
  
- **可暂停！是的！真正可暂停**<br>虽然 ffmpeg 自身并不支持暂停，但是 ntdll 可不会让着谁<br>这让你可以先暂停去奖励一下然后再继续烧机，而不是全程被硬控

- **完成后自动开始下一个**<br>你先睡觉，让它自己转

- **干净无垃圾，不保存任何信息**<br>没有用户设置，没有软件缓存，更不会碰注册表<br>不会在任何地方扔垃圾，也不会收集任何信息

## 截图

<img src="IMG\mi.png" style="zoom: 25%;" /><img src="IMG\vp.png" style="zoom: 25%;" />

## 准备步骤

1. 首先下载 3FUI，这可能会难到很多人
2. 前往 [FFmpeg 官网](https://ffmpeg.org/) 下载最新的发行版，gyan.dev 和 BtbN 两者的发行皆可
   - 若选择 gyan.dev 的发行版，应该下载 ffmpeg-release-full.7z
   - 若选择 BtbN 的发行版，应该下载 ffmpeg-master-latest-win64-gpl.zip
3. 将压缩包中的 ffmpeg.exe 和我的 FFmpegFreeUI 放在同一个文件夹中<br>或者将其加入环境变量中也可<br>
5. 然后就可以开始使用了

## 反馈

- 3FUI 没有针对酒吧的炒饭进行预防，非正常操作极易引发报错
- 故意卡 bug 造成的任何损失均与我无关
- 要反馈任何问题，请到Q群：1050613952
- **不要在 B站 汇报问题！**评论很容易被刷掉；私信也基本是让加群

### 新手必看：发生错误时如何寻求帮助

选中一个错误的任务 然后将调试信息完整地截图 然后发给技术人员！<br>最好带上命令行，如果你不想让别人看到你的文件名，可以手动抹掉或在预设管理中复制！<br>如果有条件，请提供输入文件的详细参数，很多播放器都可以查看！

> 请勿让 **我** 或 **群友** 或 **专业人士** 或 **外行人士** 进行包括但不限于这些行为：算卦、猜谜、托梦、占卜、人脑推理、强行传教、交流物理学、灵能飞升、虚空扰动、尝试进入量子隧道等等，如有以上行为或类似行为的，造成的全部后果由用户全责承担。

## 许可

- 3FUI 使用 MIT 开源许可，可以自由地使用和分发此软件
- 仅发布于 GitHub，在其他平台看到的源代码都不是本人！

## 新手入门

如果是纯新手，对视频的技术参数没有任何了解，建议先学习以下内容

- 极客湾 | 视频基础参数科普 | [BV1nt411Q7S6](https://www.bilibili.com/video/BV1nt411Q7S6)
- 极客湾 | 电影和游戏的帧数效果差别 | [BV19x411L7fH](https://www.bilibili.com/video/BV19x411L7fH)
- 影视飓风 | 视频的封装与编码 | [BV1ws41157f8](https://www.bilibili.com/video/BV1ws41157f8)
- 影视飓风 | 色深和色度采样 | [BV1ds411T7F4](https://www.bilibili.com/video/BV1ds411T7F4)
- 影视飓风 | 帧率的旧事 | [BV1hp4y1f7B5](https://www.bilibili.com/video/BV1hp4y1f7B5)
- 大河李斯特视频工作室 | 视频格式与基础参数科普 | [BV1Ug4y1L7aK](https://www.bilibili.com/video/BV1Ug4y1L7aK)
- 大河李斯特视频工作室 | 视频压缩、色度半采样、视频中的高低频 | [BV1FM41137MM](https://www.bilibili.com/video/BV1FM41137MM)
- 大河李斯特视频工作室 | FFmpeg 是什么 | [BV1SjdoY9Erj](https://www.bilibili.com/video/BV1SjdoY9Erj)
- 终末诗 | 适用于小白的视频压缩教学 | [知乎](https://zhuanlan.zhihu.com/p/1913258114746122747)

## 视频编码器

| 编码器类别 | 提供的编码                                                   | 备注                                                         |
| ---------- | ------------------------------------------------------------ | ------------------------------------------------------------ |
| 复制流     | copy                                                         |                                                              |
| H.266/VVC  | libx266<br>libvvenc                                          | 截止 2025 年，H.266 还不成熟，需要大量性能，也没几个播放器放得出来 |
| AV1        | libaom-av1<br>av1_nvenc<br>av1_qsv<br>av1_amf<br>libsvtav1<br>rav1e | 如果没有可用的新显卡进行硬件加速，强烈建议考虑软件编码 libsvtav1 |
| H.265/HEVC | libx265<br>hevc_nvenc<br>hevc_qsv<br>hevc_amf                |                                                              |
| H.264/AVC  | libx264<br>h264_nvenc<br>h264_qsv<br>h264_amf                |                                                              |
| ProRes     | prores_ks                                                    |                                                              |
| VP9        | libvpx-vp9                                                   |                                                              |
| 禁用       | -vn                                                          |                                                              |

> **新手常问：能不能显卡加速？有没有 N /A/ I 卡？**
> 答：lib = CPU，nvenc = NVIDIA，amf = AMD，qsv = INTEL，再问紫砂

## 音频编码器

复制流、AAC、LAME MP3、FLAC、ALAC、WAV 16bit、WAV 24bit、WAV 32bit Float、Dolby Digital AC3、DTS Coherent Acoustics、Opus、Vorbis、True Audio、禁用

## 图片编码器

PNG、JPEG\JPG、WEBP、TIFF、AVIF、GIF、BMP、JPEG-LS、DPX、OpenEXR

## 比特率控制方式

| 方式            | 说明                                                         |
| --------------- | ------------------------------------------------------------ |
| 动态码率 VBR    | 存储首选，硬件加速首选<br/>配合 -cq 或 -qp 使用，VBR HQ 同理 |
| 动态码率 VBR HQ | 硬件加速专用<br>仅限 NVIDIA、INTEL、AMD 的 AV1、HEVC、H264 硬件加速编码器使用<br>其他编码器选这个等同于 ABR |
| 恒定质量 CRF    | 存储首选，软件编码首选<br>-rc 并没有 crf 这个值，而是使用 -crf <?>，你需要在质量控制里填写它 |
| 恒定量化 CQP    | 不推荐，主用于研究和特定场景<br/>仅向 NVIDIA 和 AMD 的 AV1、HEVC、H264 硬件加速编码传递对应的参数<br/>其他编码器选这个等同于 ABR |
| 平均码率 ABR    | 相当于没有 -rc 参数，经典的转码                              |
| 二次编码 TPE    | 也不建议，二次编码不见得总会比单次编码好<br>只对 NVIDIA 的 HEVC 和 H264 硬件加速编码器传递参数<br>其他编码器选这个等同于 ABR |
| 恒定速率 CBR    | 应该没什么人用这玩意，我知道还有个 CBR HQ，但恒定速率对于普通人来说真没什么意义 |

### 前瞻分析帧数

建议搭配 VBR HQ 使用，通常考虑为原视频的帧率<br>AMD 的硬件加速编码器不要写这个参数，写了也不会传递，已经预置高质量参数了

### 质量设定 -crf / -cq / -qp

质量的默认值是 23，肉眼无损是 16，但仍需根据具体编码器调整<br>不要设置为 0！除非你知道自己在做什么以及需要什么

> **新手常问：要怎么选？什么对应什么？设置多少比特率才是最高画质？**
> 答：硬件加速选 VBR 和 HQ 搭配 -cq 使用，软件编码选 CRF；要想同时拥有画质和降低大小就不要想着设置比特率，去设置质量值，让编码器自己算；没有通用的方案也没有最好的方案，编码时间、画面质量、文件体积、解码性能，你总要至少放弃一样，不要想着全都要，都是按照自己的需求慢慢试出来的，只能给参考，没有作业抄。

## 视频滤镜

- 画面缩放维持比例 scale
- 画面裁剪 crop
- 智能抽帧 select='gt(scene,?)',setpts=N/FRAME_RATE/TB
- 色彩管理 zscale
- 降噪 hqdn3d、nlmeans、atadenoise、bm3d、AviSynth（avs）
- 锐化 unsharp
- 转逐行 yadif
- 转隔行 tinterlace

## 音频滤镜

- 响度标准化 loudnorm

## 如何使用画面裁剪可视化交互

<img src="IMG\sc.png"  />

画面裁剪滤镜 crop 的四个参数值是：**裁剪宽度:裁剪高度:左上角X:左上角Y**

在分辨率板块中打开此窗口，此界面独立，仅向主窗口上的那个文本框传递最终值，与已添加的文件无关。首先需要打开一个视频文件用于获取一帧预览图用来裁剪，在此之前可以设定时间戳来指定某个位置的帧，如果不设置默认获取第10秒的第一帧。此功能需要 ffmpeg 才能获取到视频帧。

获取到视频帧后，图片将以原分辨率显示，在图片上使用鼠标左右键来调整红框的尺寸，红框就是要裁剪的目标区域。左键控制左上角坐标，右键控制右下角坐标，如果按错了或者在越界的位置按下并拖动鼠标，则会自动互换功能。可以手动更改参数文本框的值然后按 Enter 键来微调红框，也就是可以反向操作。如果需要让红框保持固定比例或居中，也提供了相应的功能。在窗口右上角还有红框定位的放大镜视图，更方便精确定位。

我都写成这样了，软件里又写一遍，再不会用就去紫砂。

## 如何通过 avs 滤镜脚本文件使用 AviSynth+ 滤镜

> 本段内容由 hajimanbo 提供内容改进

AviSynth 选项在降噪设置里提供，最后一个选项就是。3FUI 只能使用 avs 文件来加载，在开始前必须明确，3FUI 是设计用于批量处理的转码工具，因此这个加载逻辑也必然是这样设计的。当使用此滤镜时，avs 文件将取代输入文件的位置，3FUI 默认您不会在 avs 里处理音频，为了避免新手直接用发现视频声音没了，因此当选择此降噪时自动覆盖填写自定义参数和流控制参数，请注意检查。

首先下载这些 dll 文件：

- AviSynth.dll（在发行版中有个名为 filesonly 的那里面找）<br>https://github.com/AviSynth/AviSynthPlus/releases
- LSMASHSource.dll<br>https://github.com/HomeOfAviSynthPlusEvolution/L-SMASH-Works/releases<br>此文件用于读取视频文件
- knlmeanscl.dll<br>https://github.com/Khanattila/KNLMeansCL/releases<br>此文件用于降噪
- fmtconv.dll<br>https://gitlab.com/EleonoreMizo/fmtconv<br>用于改变视频位深

将这些文件与 ffmpeg 放在一起！

在 3FUI 的目录下创建 AviSynth.avs 文件，此文件作为模板提供给 3FUI，在其中填写以下内容：

```vb
LoadPlugin("C:\xxxx\LSMASHSource.dll")
LoadPlugin("C:\xxxx\fmtconv.dll")
LoadPlugin("C:\xxxx\knlmeanscl.dll")
LWLibavVideoSource("<FilePath>")#读取文件中的视频流
fmtc_bitdepth(bits=16,dmode=1)#为KNLMeansCL降噪而提升位深
KNLMeansCL(d=2,a=3,s=4,h=3,channels="Y",wmode=3)#对亮度平面的降噪强度高于色度平面
KNLMeansCL(d=2,a=3,s=4,h=2,channels="UV",wmode=3)#对色度平面的降噪强度低于亮度平面
fmtc_bitdepth(bits=10,dmode=0)#为libsvtav1编码而降低位深
```

如果需要在avs中读取文件的音视频流可用以下模板

```vb
LoadPlugin("C:\xxxx\LSMASHSource.dll")
LoadPlugin("C:\xxxx\fmtconv.dll")
LoadPlugin("C:\xxxx\knlmeanscl.dll")
function LibavSource2(string path, int "atrack", 
\          int "fpsnum", int "fpsden",
\          string "format", bool "cache") 
{
    atrack   = Default(atrack, -1)
    fpsnum   = Default(fpsnum, 0)
    fpsden   = Default(fpsden,  1)
    cache    = Default(cache, true)

    format   = Default(format, "")

    video = LWLibavVideoSource(path, 
    \               fpsnum=fpsnum, fpsden=fpsden, format=format,
    \               cache=cache)
    return (atrack==-2) ? video: AudioDub(video, 
   \    LWLibavAudioSource(path, stream_index=atrack, cache=cache))
}
LibavSource2("<FilePath>")#读取文件中的音视频流。atrack - 音频轨道号，默认为自动，如果为 -2，则忽略音频。cache - 如果为 true（默认值），则创建索引文件
fmtc_bitdepth(bits=16,dmode=1)#为KNLMeansCL降噪而提升位深
KNLMeansCL(d=2,a=3,s=4,h=3,channels="Y",wmode=3)#对亮度平面的降噪强度高于色度平面
KNLMeansCL(d=2,a=3,s=4,h=2,channels="UV",wmode=3)#对色度平面的降噪强度低于亮度平面
fmtc_bitdepth(bits=10,dmode=0)#为libsvtav1编码而降低位深
```

- LoadPlugin 方法用来加载这些 dll，不需要在这里加载 AviSynth.dll<br>dll 的路径请写绝对路径！
- LWLibavVideoSource 加载视频文件，直接把第四行复制过去，3FUI 会自动替换这个文件路径
- fmtc_bitdepth 用于先为 KNLMeansCL 的降噪提升位深，而后为视频编码器的编码降低位深
- KNLMeansCL 就是降噪方法，其参数如下：

原文：https://github.com/Khanattila/KNLMeansCL/wiki/Filter-description

```c#
KNLMeansCL(clip, int d, int a, int s, float h, string channels, int wmode, float wref, clip rclip, string device_type, int device_id, bool lsb_inout, bool info)
```

| 参数名      | 说明                                                         |
| ----------- | ------------------------------------------------------------ |
| clip        | 不写                                                         |
| d           | 前后参考帧数量，d=0 使用 1 帧，d=1 使用 3 帧，n=2*d+1，以此类推，值越大降噪效果越好 |
| a           | 搜索像素半径，a=1 使用 9 像素，a=2 使用 25 像素，n=(2*a+1)^2，以此类推，值越大降噪效果越好 |
| s           | 相似半径，默认 = 4，对性能的影响很小，这取决于噪声的性质     |
| h           | 过滤强度，默认 = 1.2，值越大，去除的杂色越多                 |
| channels    | 设置要去噪的颜色通道。可能的值为 YUV、Y、UV                  |
| wmode       | 0 := Welsch weighting function has a faster decay, but still assigns positive weights to dissimilar blocks. Original Non-local means denoising weighting function.<br/>1 := Modified Bisquare weighting function to be less robust.<br/>2 := Bisquare weighting function use a soft threshold to compare neighbourhoods (the weight is 0 as soon as a given threshold is exceeded).<br/>3 := Modified Bisquare weighting function to be even more robust. |
| wref        | 默认 =  1，相对于找到的最相似像素的权重，影响滤镜输出的原始像素量 |
| rclip       | 不写                                                         |
| device_type | accelerator、cpu、gpu、auto                                  |
| device_id   | 显卡索引                                                     |
| lsb_inout   | 没必要                                                       |
| info        | 输出额外信息                                                 |

3FUI 目前不会自动删除为每个文件生成的 avs 文件，这是为了方便检查有没有正常运行。
