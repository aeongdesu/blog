---
title: "BarOverlay 사용하기"
date: 2022-06-24T09:24:58Z
tags: ["osu", "keyoverlay", "baroverlay", "키오버레이", "오버레이", "설치법"]
categories: ["강좌"]
cover:
  image: "https://user-images.githubusercontent.com/50764666/175506784-da7b75d0-8671-40c4-9aea-8d4c7bc1f8bf.gif"
---

### 가로

| __light__  |  ![](https://user-images.githubusercontent.com/50764666/175506784-da7b75d0-8671-40c4-9aea-8d4c7bc1f8bf.gif) |
:-------------------------:|:-------------------------:
| __square__  |  ![](https://user-images.githubusercontent.com/50764666/175511837-48446b84-1c9b-4b83-b26b-975e60c50907.gif) |

### 세로

|         __light__        |         __square__       |
:-------------------------:|:-------------------------:
![](https://user-images.githubusercontent.com/50764666/175511877-ac09f69d-4293-486e-9419-0ecab677df28.gif)  |  ![](https://user-images.githubusercontent.com/50764666/175511888-1979c285-3bf3-435c-bc5e-0217db7cc542.gif)

# 주의
시험 끝나고 자세히 쓸 예정

# 다운
1. 하기 전 인풋 프로그램 어떤걸 쓸건지 선택하기

  - [input-overlay](https://github.com/univrsal/input-overlay/releases)[^주의]
  - [gosumemory](https://github.com/l3lackShark/gosumemory)

    둘 다 상관 없음, 원하는거 하나 골라서 쓰셈

2. [오버레이 다운하기](https://github.com/solstice23/osu-bar-overlay/releases/latest/download/osu-bar-overlay.zip)

# 설치
1. 압축풀기
2. config.js를 열어 알아서 설정\
   **inputSource에서 하기 전에 고른 인풋 프로그램을 뭐썼는지 설정해야함**
3. OBS키고 브라우저 소스 추가하고 로컬파일 index.html 선택 후 너비 높이 잘 하고 저장
   > ![](https://user-images.githubusercontent.com/50764666/175510301-8d543bee-da9f-4962-aaac-74414bb21304.png)
4. 끝

# 팁
light에서 fade가 안돼는 버그?가 있는데 브라우저 소스 속성에서 CSS부분에 **싹다 지우고**
```css
body {
background-color: rgba(0, 0, 0, 0); margin: 0px auto; overflow: hidden;
-webkit-mask-image: linear-gradient(-90deg, rgba(0,0,0,1) 0%, rgba(0,0,0,1) 75%, rgba(0,0,0,0) 100%);
		mask-image: linear-gradient(-90deg, rgba(0,0,0,1) 0%, rgba(0,0,0,1) 75%, rgba(0,0,0,0) 100%);
}
```
넣으면 됨

이건 그냥 복붙한거라 작동만 되면 그만이지

[^주의]:- 5.0 다운하셈 윈도우면 .exe 다운해서 설치하는게 빠름
    - 나는 이상하게 이거 쓰고 브라우저 소스 속성 만지작 하면 마우스 커서가 심각하게 끊기는 증상이 나옴 혹시 모르니 gosumemory 쓰든가\
    **웹소켓을 활성화 해야 작동함**
    1. 설치하고 OBS 켜서 도구 -> input-overlay settings 클릭\
    ![](https://user-images.githubusercontent.com/50764666/175508807-e97662fb-ebef-4c40-9c92-9f453f581414.png)
    2. 웹소켓 옵션 키고 확인\
    ![](https://user-images.githubusercontent.com/50764666/175508952-11fda8f6-4156-4be5-a436-f55ea146c305.png)
