# alsa 工具使用介绍

alsa-utils库中包含了多个命令行工具，比如aplay,arecord,amixer,alsamixer等，本章节会对常用的几个工具做介绍。

# 播放工具-aplay

aplay是alsa内置的音频播放工具，它的源代码位于`alsa/alsa-utils/aplay`目录，aplay可以播放裸的音频文件，比如pcm格式或者raw格式。
aplay的主要参数可通过`aplay -h`查看，如下:
```
Usage: aplay [OPTION]... [FILE]...

-h, --help              帮助信息 
    --version           打印版本信息
-l, --list-devices      列出所有的声卡及数字音频设备
-L, --list-pcms         列出所有的设备名称
-D, --device=NAME       通过名称选择PCM设备
-q, --quiet             安静模式
-t, --file-type TYPE    文件类型(voc, wav, raw or au)
-c, --channels=#        通道数 
-f, --format=FORMAT     采样格式(大小写不敏感)
-r, --rate=#            采样率 
-d, --duration=#        在# 秒钟后终止
-M, --mmap              mmap 流
-N, --nonblock          非阻塞模式 
-F, --period-time=#     中断的间隔为# 毫秒 
-B, --buffer-time=#     buffer 的持续时间是# 毫秒
    --period-size=#     中断的间隔为 # 帧
    --buffer-size=#     buffer 的持续时间为# 帧
-A, --avail-min=#       唤醒的最小时间为# 毫秒
-R, --start-delay=#     PCM 自动开始时的延迟时间为 # 毫秒 
                        (如果 <= 0则与buffer size相关)
-T, --stop-delay=#      PCM自动停止的延迟时间为 # 毫秒
-v, --verbose           show PCM structure and setup (accumulative)
-V, --vumeter=TYPE      enable VU meter (TYPE: mono or stereo)
-I, --separate-channels one file for each channel
-i, --interactive       allow interactive operation from stdin
-m, --chmap=ch1,ch2,..  Give the channel map to override or follow
    --disable-resample  disable automatic rate resample
    --disable-channels  disable automatic channel conversions
    --disable-format    disable automatic format conversions
    --disable-softvol   disable software volume control (softvol)
    --test-position     test ring buffer position
    --test-coef=#       test coefficient for ring buffer position (default 8)
                        expression for validation is: coef * (buffer_size / 2)
    --test-nowait       do not wait for ring buffer - eats whole CPU
    --max-file-time=#   start another output file when the old file has recorded
                        for this many seconds
    --process-id-file   write the process ID here
    --use-strftime      apply the strftime facility to the output file name
    --dump-hw-params    dump hw_params of the device
    --fatal-errors      treat all errors as fatal

可识别的采样格式为: S8 U8 S16_LE S16_BE U16_LE U16_BE S24_LE S24_BE U24_LE U24_BE S32_LE S32_BE U32_LE U32_BE FLOAT_LE FLOAT_BE FLOAT64_LE FLOAT64_BE IEC958_SUBFRAME_LE IEC958_SUBFRAME_BE MU_LAW A_LAW IMA_ADPCM MPEG GSM SPECIAL S24_3LE S24_3BE U24_3LE U24_3BE S20_3LE S20_3BE U20_3LE U20_3BE S18_3LE S18_3BE U18_3LE U18_3BE G723_24 G723_24_1B G723_40 G723_40_1B DSD_U8 DSD_U16_LE DSD_U32_LE DSD_U16_BE DSD_U32_BE
下面这些在一些硬件上可能无法使用,可用的格式缩写为:
-f cd (16位小端, 44100, 立体声)
-f cdr (16 位大端, 44100, 立体声)
-f dat (16 位小端, 48000, 立体声)

```

# 录音工具-arecord

# 混音工具-amixer

# 图形交互工具-alsamixer
