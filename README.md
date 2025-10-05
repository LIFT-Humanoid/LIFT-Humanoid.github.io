ffmpeg -i t1_mj_rough.mp4 -vcodec libx264 -crf 23 -preset medium -acodec aac -b:a 128k t1_mj_rough_comp.mp4

ffmpeg -i t1_mj_rough.mp4 -c:v libvpx-vp9 -b:v 0 -crf 30 -c:a libopus t1_mj_rough_comp.webm

ffmpeg -i input.mp4 -vf "fps=10,scale=640:-1:flags=lanczos" -gifflags -offsetting -y output.gif



ffmpeg -i xxx.mov -vf "fps=10,scale=640:-1:flags=lanczos" -gifflags -offsetting -y           xxx.gif
