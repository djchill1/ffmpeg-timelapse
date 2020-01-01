### Convert sequence of JPEG images to MP4 video
for creating timelapses from jpegs in ffmpeg


```
ffmpeg -r 24 -start_number 1447 -i GOPR%04d.JPG -s hd1080 -vcodec libx264 timelapse.mp4
```

* `-r` framerate
* `-start_number` the starting file number
* `-i` the input. `%04d` in the input means a 4 digit number with leading zeros. I.e. one would be 0001.
