## flv hsl stream media server

## use
```bash

## 开启node服务
node src/index.js

## 推流
./ffmpeg -re -stream_loop -1 -i 1080_h265.mp4 -c:a copy -c:v libx265 -f flv rtmp://localhost:1935/live/h265

## 播放地址
[http://lovalhost:1935/live/h265](http://localhost:8000/live/h265.flv)

```