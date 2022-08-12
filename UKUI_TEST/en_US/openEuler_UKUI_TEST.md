
English | [简体中文](../zh_CN/openEuler_UKUI_TEST_cn.md)



# Tools
## Kylin Recorder
Kylin Recorder provides a simple audio recording function, It supports microphone recording, multi audio format recording such as MP3 and WAV, and supports file list playing, deleting, mini mode and other functions to meet your recording needs in multiple directions. as shown in Fig 1.

![Fig 1 Kylin recorder-big](image/tools/kylin-recorder/recorder1.png)

### test case:
|**Number**|**Test item**|**Test steps**|**Expected results**|
| --- | --- | --- | --- |
|1|Recording|1.Click ![](image/tools/kylin-recorder/recorder2.png) recording button to enter recording interface|1.Click the recording button to generate the waveform diagram in real time|
|||2.During recording, click ![](image/tools/kylin-recorder/recorder3.png) pause recording button|2.Click the pause recording button to pause recording|
|||3.Click ![](image/tools/kylin-recorder/recorder4.png) continue recording button|3.Click the continue recording button to continue recording|
|||4.Click ![](image/tools/kylin-recorder/recorder5.png) stop button to finish recording|4.Automatically generate audio files in the file list|
|2|Playing|1.Select any file in the file list and click ![](image/tools/kylin-recorder/recorder6.png) play button|1.The selected file plays normally|
|||2.Click ![](image/tools/kylin-recorder/recorder7.png) delete file button|2.The selected file is deleted normally|
|3|Setting|1.Click ![](image/tools/kylin-recorder/recorder8.png) setting button to customize the storage path and select the recording file format|1.Can be set normally|
|4|mini|1.Click ![](image/tools/kylin-recorder/recorder9.png) mini button to enter the mini mode and click ![](image/tools/kylin-recorder/recorder10.png) restore button to switch back to the original interface|1.The mini mode and the original interface can be switched normally|

