# How to use

prepare ffmpeg & ab-av1 exe file

Run index.html

0. Add environment variable Paths of ffmpeg / ab-av1
  Or paste the paths in '(optional)' inputs
1. Copy your videos' Paths in File Explorer (Ctrl + Shift + C)
2. Paste in 'Paste Your Paths' and (optional) type CRFs
3. Set your Option
4. Copy the result and Run in CMD

<img src="https://github.com/parkjonghyukp/park/assets/149362146/c7b62a24-bf08-49b0-b983-2aa593a52b90" alt="image01"/>


#### Full result query of the image might be
```cmd
ab-av1 auto-encode -e svt-av1 -i "2023-12-17 17-01-31.mp4" --preset 5 && ab-av1 auto-encode -e svt-av1 -i "2023-12-17 17-01-33.mp4" --preset 5 && ffmpeg -i "2023-12-17 17-01-31.av1.mp4" -c:v copy -c:a libopus -b:a 96K "2023-12-17 17-01-31_opus.mp4" && del "2023-12-17 17-01-31.av1.mp4" && ffmpeg -i "2023-12-17 17-01-33.av1.mp4" -c:v copy -c:a libopus -b:a 96K "2023-12-17 17-01-33_opus.mp4" && del "2023-12-17 17-01-33.av1.mp4" && shutdown -s -f -t -30
```
