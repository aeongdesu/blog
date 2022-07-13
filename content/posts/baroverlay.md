---
title: "BarOverlay 사용하기"
date: 2022-06-24T09:24:58Z
tags: ["osu", "keyoverlay", "baroverlay", "키오버레이", "오버레이", "설치법"]
categories: ["강좌"]
cover:
  image: "https://user-images.githubusercontent.com/50764666/175506784-da7b75d0-8671-40c4-9aea-8d4c7bc1f8bf.gif"
---
# 미리보기

### 가로

| __light__  |  ![](https://user-images.githubusercontent.com/50764666/175506784-da7b75d0-8671-40c4-9aea-8d4c7bc1f8bf.gif) |
:-------------------------:|:-------------------------:
| __square__  |  ![](https://user-images.githubusercontent.com/50764666/175511837-48446b84-1c9b-4b83-b26b-975e60c50907.gif) |

### 세로

|         __light__        |         __square__       |
:-------------------------:|:-------------------------:
![](https://user-images.githubusercontent.com/50764666/175511877-ac09f69d-4293-486e-9419-0ecab677df28.gif)  |  ![](https://user-images.githubusercontent.com/50764666/175511888-1979c285-3bf3-435c-bc5e-0217db7cc542.gif)

# 잡담
많이 쓰는 [KeyOverlay](https://github.com/Blondazz/KeyOverlay)가 이미 있는데, 프로그램을 하나 더 실행하는것이라 귀찮음이 있습니다.. 🙄\
그래서 깃헙을 찾아보니 인풋 프로그램만 있으면 OBS에 브라우저 소스만 넣어도 가능한 BarOverlay를 찾았습니다.

# 다운
1. 하기 전 인풋 프로그램 선택
  - [input-overlay](https://github.com/univrsal/input-overlay/releases)[^주의]
  - [gosumemory](https://github.com/l3lackShark/gosumemory)
  > 둘 다 상관 없습니다, 원하는거 하나 골라서 쓰시면 됩니다.

2. [오버레이 다운](https://github.com/solstice23/osu-bar-overlay/releases/latest/download/osu-bar-overlay.zip)

# 설치
1. 압축 풀기
2. config.js를 열어 알맞게 설정
   > **inputSource에서 다운할때 고른 인풋 프로그램을 어떤걸 사용했는지 설정해야 합니다.**
3. OBS 실행 후 브라우저 소스 추가하고 로컬파일 index.html 선택 후 너비, 높이 알맞게 수정 후 저장
   > ![](https://user-images.githubusercontent.com/50764666/175510301-8d543bee-da9f-4962-aaac-74414bb21304.png)

# 버그?
light에서 fade가 안돼는 버그?가 있는데 브라우저 소스 속성에서 CSS 부분에 **전부 지우시고**
```css
body {
background-color: rgba(0, 0, 0, 0); margin: 0px auto; overflow: hidden;
-webkit-mask-image: linear-gradient(-90deg, rgba(0,0,0,1) 0%, rgba(0,0,0,1) 75%, rgba(0,0,0,0) 100%);
		mask-image: linear-gradient(-90deg, rgba(0,0,0,1) 0%, rgba(0,0,0,1) 75%, rgba(0,0,0,0) 100%);
}
```
해당 코드를 넣으시고 저장하시면 됩니다.

###### ~~css에 있는 코드를 복붙하였습니다, 작동하면 그만이죠~~

[^주의]:- 5.0 버전을 다운해주세요, 윈도우면 .exe 다운해서 설치하는게 빠릅니다.
    - 저는 이상하게 설치 후 브라우저 소스 속성에서 가만히 있으면 마우스 커서가 심각하게 끊기는 증상이 생깁니다. (obs를 끄면 해결) 혹시 모르니 gosumemory를 쓰시는게 좋습니다.\
    **웹소켓을 활성화 해야 작동합니다!**

    1. 설치하고 OBS 실행 후 `도구` -> `input-overlay settings` 클릭\
   ![](https://user-images.githubusercontent.com/50764666/175508807-e97662fb-ebef-4c40-9c92-9f453f581414.png)
    2. 웹소켓 옵션 키고 확인\
   ![](https://user-images.githubusercontent.com/50764666/175508952-11fda8f6-4156-4be5-a436-f55ea146c305.png)
