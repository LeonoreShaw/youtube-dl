# youtube-dl使用简介（网速限制==已死==）

 列出视频和音频可选品质

```
youtube-dl -F url
```

选择相应品质前的序号，最后是视频的地址

```
youtube-dl -f 313+251 https://youtu.be/3pYsfaQeMRs
```

最高品质下载并转换格式

```
youtube-dl -f bestvideo+bestaudio --merge-output-format mkv https://youtu.be/3pYsfaQeMRs
```

下载的视频保存在`youtube-dl.exe`同级文件夹下

 

## aria2多线程下载

16线程，1M块大小

```
youtube-dl -f bestvideo+bestaudio --merge-output-format mkv https://youtu.be/3pYsfaQeMRs --external-downloader aria2c --external-downloader-args "-x 16  -k 1M"
```



## 快捷下载最高MP4

```
youtube-dl -f 22 url --external-downloader aria2c --external-downloader-args "-x 16 -k 1M"
```









# youtube-dlp下载(外网)

# ==进入youtubedlp目录下操作==

 列出视频和音频可选品质

```
yt-dlp -F url
```

选择相应品质前的序号，最后是视频的地址

```
yt-dlp -f 137 url
```

### 快捷下载最高MP4

```
yt-dlp -f 22 url --external-downloader aria2c --external-downloader-args "-x 16 -k 1M"
```





# 综上，CMD下使用yt_dlp下载

1、进入youtubedlp目录下运行CMD

2、列出视频和音频可选品质

```
yt-dlp -F url
```

3、选择相应品质前的序号,保存在aria2的config选择的目录

```
yt-dlp -f 400 url --external-downloader aria2c --external-downloader-args "-x 16 -k 1M"
```









# 快速下载方式
1、==进入youtubedlp目录下运行==

2、列出视频和音频可选品质

```
yt-dlp -F https://youtu.be/3pYsfaQeMRs
```

![image-20211111212344354](https://gitee.com/leonoreshaw/Images/raw/ReadmeFilesImages/youtube-dl/Snipaste_2021-11-11_21-50-12.png)

3、选择相应品质前的序号,保存在同级目录下

244为仅视频+251为仅音频，转码为MP4

```
yt-dlp -f 313+251 --merge-output-format mp4 https://youtu.be/3pYsfaQeMRs
```

![image-20211111213138849](https://gitee.com/leonoreshaw/Images/raw/ReadmeFilesImages/youtube-dl/Snipaste_2021-11-11_21-55-05.png)

其他：

仅视频（没声音）或仅音频

```
yt-dlp -f 400 url
```

或使用aria2多线程下载

```
yt-dlp -f 313+251 https://youtu.be/3pYsfaQeMRs --external-downloader aria2c --external-downloader-args "-x 16 -k 1M"
```

![image-20211111213138849](https://gitee.com/leonoreshaw/Images/raw/ReadmeFilesImages/youtube-dl/Snipaste_2021-11-11_21-59-38.png)



![image-20211111213138849](https://gitee.com/leonoreshaw/Images/raw/ReadmeFilesImages/youtube-dl/Snipaste_2021-11-11_22-01-46.png)



###  CMD命令

```
yt-dlp -F https://youtu.be/3pYsfaQeMRs
yt-dlp -f 313+251 --merge-output-format mp4 https://youtu.be/3pYsfaQeMRs --external-downloader aria2c --external-downloader-args "-x 16 -k 1M"
```

