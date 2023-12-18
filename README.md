# ab-av1-encoding-util
#### batch generator using ffmpeg & ab-av1
![image](https://github.com/parkjonghyukp/ab-av1-encoding-util/assets/149362146/6642eb25-491d-40b1-ac73-92e677a9f4a2)


# How to use

prepare ffmpeg & ab-av1 exe file

Run index.html

0. Add environment variable Paths of ffmpeg / ab-av1
  Or paste the paths in '(optional)' inputs
1. Copy your videos' Paths in File Explorer (Ctrl + Shift + C)
2. Paste in 'Paste Your Paths' and (optional) type CRFs
3. Set your Option
4. Copy the result and Run in CMD

# Examples
<img src="https://github.com/parkjonghyukp/park/assets/149362146/c7b62a24-bf08-49b0-b983-2aa593a52b90" alt="image01"/>


#### result of above image might be
```cmd
ab-av1 auto-encode -e svt-av1 -i "2023-12-17 17-01-31.mp4" --preset 5 && ab-av1 auto-encode -e svt-av1 -i "2023-12-17 17-01-33.mp4" --preset 5 && ffmpeg -i "2023-12-17 17-01-31.av1.mp4" -c:v copy -c:a libopus -b:a 96K "2023-12-17 17-01-31_opus.mp4" && del "2023-12-17 17-01-31.av1.mp4" && ffmpeg -i "2023-12-17 17-01-33.av1.mp4" -c:v copy -c:a libopus -b:a 96K "2023-12-17 17-01-33_opus.mp4" && del "2023-12-17 17-01-33.av1.mp4" && shutdown -s -f -t -30
```

![image](https://github.com/parkjonghyukp/ab-av1-encoding-util/assets/149362146/ed6bc04d-8af2-49a2-bc7f-45da38c1aac1)


#### result of above image might be
```cmd
ab-av1 encode -e hevc_nvenc -i "C:\Users\User\Videos\2023-12-17 17-01-31.mp4" --crf 34 --preset 5 && ab-av1 encode -e hevc_nvenc -i "C:\Users\User\2023-12-17 17-01-33.mp4" --crf 34 --preset 5 && ffmpeg -i "C:\Users\User\Videos\2023-12-17 17-01-31.hevc_nvenc.mp4" -c:v copy -c:a libopus -b:a 96K "C:\Users\User\Videos\2023-12-17 17-01-31_opus.mp4" && del "C:\Users\User\Videos\2023-12-17 17-01-31.hevc_nvenc.mp4" && ffmpeg -i "C:\Users\User\2023-12-17 17-01-33.hevc_nvenc.mp4" -c:v copy -c:a libopus -b:a 96K "C:\Users\User\2023-12-17 17-01-33_opus.mp4" && del "C:\Users\User\2023-12-17 17-01-33.hevc_nvenc.mp4" && shutdown -s -f -t -30
```
