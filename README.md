# Local-Promo-Cards
A promotional card generator for your local music files, for sharing on social media.

You use it in conjunction with https://www.onlineconverter.com/audio-to-video to get audio and the just generated image merged into a single video container. That you can now share wherever you like.

As a general rule, social nedia apps tend to cap the length of media files. WhatsApp has the annoying 90s cap for video content. In this case you'll have to split. I'm currently looking for a web solution that uses ffmpeg under the hood as that would be an optimal solution. In the meantime, use this command:

```sh
ffmpeg -i input_video.mp4 -map 0 -c copy -f segment -segment_time <length in seconds/number of segments> -reset_timestamps 1 part_%03d.mp4
```
