### http
chunk
- 可以把一个http请求分多次到达
Range & Content-Range
- 可以获取指定的然个内容
### 流媒体协议
常用的流媒体协议主要有 HTTP 渐进下载和基于 RTSP/RTP 的实时流媒体协议，这二种基本是完全不同的东西
- HTTP渐进式：如YouTube、优酷等大型视频网站的点播分发。它的核心区别是媒体文件不分片，直接以完整文件形态进行分发，通过支持Seek,终端播放器可从没下载完成部分中任意选取一个时间点开始播放，如此来满足不用等整个文件下载完快速播放的需求，一般MP4和FLV格式文件支持较好，打开一个视频拖拽到中部，短暂缓冲即可播放，点击暂停后文件仍将被持续下载就是典型的渐进式下载。
- HLS类“伪”HTTP流：HLS（Apple）、HDS(Adobe)、MSS(Microsoft) 、DASH（MPEG组织）均属于“伪”HTTP流，之所以说他们“伪”，是因为他们在体验上类似“流”，但本质上依然是HTTP文件下载。以上几个协议的原理都一样，就是将媒体数据（文件或者直播信号）进行切割分块，同时建立一个分块对应的索引表，一并存储在HTTP Web服务器中，客户端连续线性的请求这些分块小文件，以HTTP文件方式下载，顺序的进行解码播放，我们就得到了平滑无缝的“流”的体验。
- HTTP流：http-flv这样的使用类似RTMP流式协议的HTTP长连接，需由特定流媒体服务器分发的，是真正的HTTP流媒体传输方式，他在延时、首画等体验上跟RTMP等流式协议拥有完全一致的表现，同时继承了部分HTTP的优势。
### 流的本质是把一个整体拆分成小分
- 流可以同步读取-磁盘内存数组等
- 也可以异步来到如网络等