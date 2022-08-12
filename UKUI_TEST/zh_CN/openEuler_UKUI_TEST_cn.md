
[English](../en_US/openEuler_UKUI_TEST.md) | 简体中文



# 小工具
## 麒麟录音
麒麟录音，是一款界面友好操作简单的录音工具，支持麦克风录制，多音频格式录制如mp3、wav等，支持文件列表播放、删除以及迷你模式等功能，多方位满足您的录音需求。主界面如图录音1所示。

![图录音1 麒麟录音-big](image/tools/kylin-recorder/recorder1_cn.png)

### 测试用例：
|**编号**|**测试项**|**测试步骤**|**期望结果**|
| --- | --- | --- | --- |
|1|录音|1.点击 ![](image/tools/kylin-recorder/recorder2_cn.png) 录音按钮开始录音|1.点击录音按钮，实时生成波形图|
|||2.录音过程中，点击 ![](image/tools/kylin-recorder/recorder3_cn.png) 暂停录音按钮|2.点击暂停录音按钮，暂停录音|
|||3.再继续点击 ![](image/tools/kylin-recorder/recorder4_cn.png) 继续录音按钮|3.点击继续录音按钮，继续录音|
|||4.点击 ![](image/tools/kylin-recorder/recorder5_cn.png) 停止按钮完成录音|4.自动在文件列表中生成音频文件|
|2|播放|1.选中文件列表中的任意一个文件，点击 ![](image/tools/kylin-recorder/recorder6_cn.png) 播放按钮|1.选中的文件正常播放|
|||2.点击 ![](image/tools/kylin-recorder/recorder7_cn.png) 删除文件按钮|2.选中的文件正常删除|
|3|设置|1.点击 ![](image/tools/kylin-recorder/recorder8_cn.png) 设置按钮，用户可自定义存储路径，选择录音文件格式|1.可以正常设置|
|4|迷你模式|1.点击 ![](image/tools/kylin-recorder/recorder9_cn.png) 迷你按钮可进入迷你模式，点击 ![](image/tools/kylin-recorder/recorder10_cn.png) 复原按钮切回原界面|1.迷你模式和原界面可以正常切换|

