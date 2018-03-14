copy pasta draft from *.txt

# get file metadata
ffprobe -i input.mp4 -show_streams

# test if a file is mjpeg
ffprobe -v error -select_streams v:0 -show_entries stream=codec_name -of default=nw=1 input.avi 

# extract lossless as jpeg
ffmpeg -i input.avi -codec:v copy -bsf:v mjpeg2jpeg output_%03d.jpg

# If you use -ss after -i, you get more accurate seeking at the expense of slower execution altogether. You can also put -ss before -i.
# See also: Seeking with FFmpeg
# This is no longer true as of FFmpeg 2.1; the location of -ss will not affect the accuracy of the encode. However, 

# clip start 
-ss 00:00:30.0

# 2x vertical scale
-qscale:v 2

# extract as images
ffmpeg -i input.mp4 output_%04d.jpg

# using seek to clip
ffmpeg -i video.mp4 -ss 00:00:16 -to 00:01:45 output_%04d.jpg

# change aspect ratio without reencoding
ffmpeg -i file.mp4 -c copy -aspect 1.5 <out.mp4  

# stream specific window
ffmpeg -f gdigrab -framerate 30 -i title="specific window title" -b:v 3M  out.flv

# stream desktop
ffmpeg -f gdigrab -framerate 12 -i desktop out.mp4
ffmpeg -f gdigrab -framerate 6 -i desktop out.mpg

# loop vid from a static image
ffmpeg -loop 1 -i output_0015.jpg -c:v libx264 -t 2 vid_loop.mp4

# concatenate two videos
    # 1. move to intermediate format *.ts
    ffmpeg -i vid_loop.mp4 -c copy -bsf:v h264_mp4toannexb -f mpegts input1.ts
    ffmpeg -i trackvis_files_w_GLiDE_Pointset.mp4 -c copy -bsf:v h264_mp4toannexb -f mpegts input2.ts
    # 2. concatenate*.ts
    ffmpeg -i "concat:input1.ts|input2.ts" -c copy demo_vid.mp4

# reencode to share with windows media player users (!)
ffmpeg  -i video.mp4 -pix_fmt yuv420p win_player_friendly_out.mp4 