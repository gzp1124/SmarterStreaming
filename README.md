# SmarterStreaming
SmarterStreaming系列产品，系daniulive（大牛直播）出品的跨平台视频采集、直播SDK（支持私有协议和RTMP推流，如windows推流/android推流/iOS推流/windows播放/android播放/iOS播放），公网毫秒级延迟，也许是国内最靠谱的视频直播推流、播放SDK之一，助您轻松实现类似于花椒、映客、斗鱼手机直播推送与播放。

<img src="http://daniulive.com:8080/files/image/SmarterStreaming.png" width="313" alt="SmarterStreaming" />

**[一对一实时音视频互动]**

1. 基于P2P或流媒体转发的一对一音视频互动产品；
2. 以秀场、在线教育、远程诊疗、智能门禁等为核心的跨平台音视频实时互动。

**[一对多，多对多直播、互动]**

1. windows推流：Windows端实时采集，支持屏幕采集和摄像头采集；
2. windows播放器：Windows端实时播放（支持同时直播多画面，支持CS架构播放和无需安装第三方插件的浏览器端播放）；
3. android推流：Android端实时采集（支持多分辨率采集、采集过程中，前后摄像头切换）；
4. android播放器：Android端实时播放（支持超低延迟播放多路直播视频）；
5. iOS推流：iOS端实时采集（支持多分辨率采集、采集过程中，前后摄像头切换）；
6. iOS播放器：iOS端实时播放（支持超低延迟播放多路直播视频）；
7. 支持微信公众账号集成（RTMP输入，HLS播放）；
8. 公网环境下，**毫秒级延迟**，支持云服务部署、各类厂商的CDN产品对接；
9. 支持边推送边录像（如执法记录或移动单兵场景），网络中断仍可继续录制，结束后可本地回放，并可对接第三方云服务，把录像数据保存到云端服务器。

**[基于RTMP安防摄像机平台对接]**

高稳定性、超低延迟的跨平台（Windows/android/iOS）综合视频监控系统对接。

**[多对一实时通讯]**

适用于应急指挥、公安巡检等，以移动单兵设备为采集载体，实时上传音视频数据到指挥中心，并实现指挥中心对现场的实时指导。

您可以用网页进行播放测试：<a href="http://daniulive.com:8080/files/SmartPlayer/SmartPlayer.html" target="_blank">http://daniulive.com:8080/files/SmartPlayer/SmartPlayer.html</a>

**SmarterStreaming SDK库个人使用免费，企业及商用需要经过授权**；

## 公网环境下推流、直播效果展示 ##
<img src="http://daniulive.com:8080/files/image/WindowsPublisher.JPG" width="800" alt="Windows采集，跨平台播放" />

<img src="http://daniulive.com:8080/files/image/AndroidPublisher.JPG" width="800" alt="Android采集，跨平台播放" />

<img src="http://daniulive.com:8080/files/image/IOSPublisher.JPG" width="800" alt="iOS采集，跨平台播放" />

## RTMP摄像机对接 ##
**1. Windows播放端：**
<img src="http://daniulive.com:8080/files/image/windowscameradisplayer.JPG" width="800" alt="RTMP摄像机播放" />

**2. Android播放端：**
<img src="http://daniulive.com:8080/files/image/androidcameradisplayer.JPG" width="800" alt="android端播放RTMP摄像机数据" />

**3. iOS播放端：**
<img src="http://daniulive.com:8080/files/image/iOScameradisplayer.JPG" width="800" alt="iOS端播放RTMP摄像机数据" />

**4. 边推送边录像：**
<img src="http://daniulive.com:8080/files/image/localrecorder.JPG" width="800" alt="边推送边录像" />

## 使用说明 ##

**1. 推流:**

**1.1 Windows端推流：**

选择“WindowsPusher&Player”文件，打开“SmartClientDemo.exe”（如需推送桌面，请使用SmartClientDeskDemo.exe，默认会采集PC屏幕左上角一块区域），进入系统后，左侧系推流端，右侧是播放端，推流依次点击:

1. Open;
2. Login（输入用户名、密码)，如需Windows端推流测试，请联系QQ 89030985，或加入QQ群 499687479 和群主联系;
3. 输入用户名、密码之后，会自动根据用户名生成对应的播放URL，如用户名daniulive，则生成的url为：rtmp://daniulive.com:1935/hls/streamdaniulive;
4. 点击PushStream，完成Windows推流。

PushStream，如推流成功的话，会显示推流地址，如本URL对应的链接为：
rtmp://daniulive.com:1935/hls/streamdaniulive.

**1.2 Android端推流：**

安装SmartPublisher， 进入系统后，会自动生成urlID, 如 rtmp://daniulive.com:1935/hls/stream123456, 对应的urlID即为 123456（stream后的数字），点击“开始推流”，推流过程中，可点击右上角“切换前后摄像头”图标；来切换视角进行采集；

**1.3 移动端边推送边录像：**

以Android推流端为例，“开始推流”之前，选择“本地录像”，然后点推流，推流结束后，会自动在本地录制推流音视频（mp4文件），并可到“录像管理”页面，查看本地录制文件，单击文件名，即可完成本地文件播放。

**2 播放：**

**2.1 Windows播放：**

选择“WindowsPusher&Player”文件，打开“SmartClientDemo.exe”，右侧输入框输入 rtmp://daniulive.com:1935/hls/stream123456;， 然后依次点击 PlayerOpen-->StartPlay即可。

**2.2 SmartPlayer.apk(android为例)**

进入系统后，点击“输入urlID”，在弹出的对话框输入"123456"(也就是分配的账号)，点击开始播放即可，停止的话，点击停止播放即可。

**2.3 Web播放**

http://daniulive.com:8080/files/SmartPlayer1Stream/SmartPlayer.html

在输入框中，清除老的url，输入推流的url，如 rtmp://daniulive.com:1935/hls/stream123456（以推流端生成的URL为准）。


## 获取更多信息 ##

商务合作：QQ：89030985 
技术支持：QQ: 2679481035

QQ群(大牛直播技术交流群)：499687479

<img src="http://daniulive.com:8080/files/image/erweima.png" width="302" alt="QQ交流群" />
