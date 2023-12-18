# ab-av1-batch-util
#### batch code generator of ffmpeg & ab-av1

#### ab-av1 다중 파일 코드 생성기
![image](https://github.com/parkjonghyukp/ab-av1-encoding-util/assets/149362146/6642eb25-491d-40b1-ac73-92e677a9f4a2)

</br></br>

# Requirement / 요구사항

* [ffmpeg](https://github.com/FFmpeg/FFmpeg)
* [ab-av1](https://github.com/alexheretic/ab-av1)
* (Optional / 선택사항) [Powershell](https://github.com/PowerShell/PowerShell)

</br></br>

# How to use

Run index.html

0. Add environment variable Paths of ffmpeg / ab-av1, or paste the paths in '(optional)' inputs
1. Copy your videos' Paths in File Explorer (Ctrl + Shift + C)
2. Paste in 'Paste Your Paths' and (optional) type CRFs
3. Set your Option, copy the result and Run in cmd / Powershell

Note : if the result is larger than 5Kb, use [Powershell](https://github.com/PowerShell/PowerShell) latest version

# 사용법

index_ko.html 실행

0. ab-av1와 ffmpeg의 환경 변수 추가하거나, '(선택사항)' 입력란에 파일 위치 추가하기
1. 영상 경로 복사 (Ctrl + Shift + C)
2. '비디오 경로'에 경로 붙여 넣기
3. 옵션 설정 후 cmd / Powershell에 결과 붙여넣고 실행

참고 : 결과가 5Kb 보다 클 경우 [Powershell](https://github.com/PowerShell/PowerShell) 최신버전을 사용하시오

</br></br>

# Examples / 예시
<img src="https://github.com/parkjonghyukp/park/assets/149362146/c7b62a24-bf08-49b0-b983-2aa593a52b90" alt="image01"/>

</br>

#### result of above image might be / 위 사진의 결과는

```cmd
ab-av1 auto-encode -e svt-av1 -i "2023-12-17 17-01-31.mp4" --preset 5 && ab-av1 auto-encode -e svt-av1 -i "2023-12-17 17-01-33.mp4" --preset 5 && ffmpeg -i "2023-12-17 17-01-31.av1.mp4" -c:v copy -c:a libopus -b:a 96K "2023-12-17 17-01-31_opus.mp4" && del "2023-12-17 17-01-31.av1.mp4" && ffmpeg -i "2023-12-17 17-01-33.av1.mp4" -c:v copy -c:a libopus -b:a 96K "2023-12-17 17-01-33_opus.mp4" && del "2023-12-17 17-01-33.av1.mp4" && shutdown -s -f -t -30
```

![image](https://github.com/parkjonghyukp/ab-av1-encoding-util/assets/149362146/ed6bc04d-8af2-49a2-bc7f-45da38c1aac1)



#### result of above image might be / 위 사진의 결과는

```cmd
ab-av1 encode -e hevc_nvenc -i "C:\Users\User\Videos\2023-12-17 17-01-31.mp4" --crf 34 --preset 5 && ab-av1 encode -e hevc_nvenc -i "C:\Users\User\2023-12-17 17-01-33.mp4" --crf 34 --preset 5 && ffmpeg -i "C:\Users\User\Videos\2023-12-17 17-01-31.hevc_nvenc.mp4" -c:v copy -c:a libopus -b:a 96K "C:\Users\User\Videos\2023-12-17 17-01-31_opus.mp4" && del "C:\Users\User\Videos\2023-12-17 17-01-31.hevc_nvenc.mp4" && ffmpeg -i "C:\Users\User\2023-12-17 17-01-33.hevc_nvenc.mp4" -c:v copy -c:a libopus -b:a 96K "C:\Users\User\2023-12-17 17-01-33_opus.mp4" && del "C:\Users\User\2023-12-17 17-01-33.hevc_nvenc.mp4" && shutdown -s -f -t -30
```
