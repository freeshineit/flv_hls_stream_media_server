## flv hsl stream media server

## use
```bash

## 开启node服务
node src/index.js

## 推流并转换视频和音频编码
ffmpeg -re -stream_loop -1 -i 1080.mp4 -c:a copy -c:v libx264 -f hls rtmp://localhost:1935/live/h265

## 播放地址
[http://localhost:8000/live/h265.flv](http://localhost:8000/live/h265.flv)


## 
# ffmpeg -re stream_loop -1 -i 1080.mp4 -c copy -f hls rtmp://localhost/live/STREAM_NAME

# [http://lovalhost:8000/live/STREAM_NAME/index.m3u8](http://localhost:8000/live/hls/index.m3u8)
```