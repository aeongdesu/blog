---
title: "Spotify 데스크톱 클라이언트를 새로운 UI로 변경하기"
date: 2021-04-12T19:53:55+09:00
description: "다른 사람들은 새로운 UI가 적용되어 있는데 왜 내 Spotify는 구 UI지?"
tags: ["스포티파이", "Spotify", "UI", "적용법"]
categories: ["강좌"]
cover:
  image: "https://nyan.shx.gg/cA2E9C.png"
---

# 잡담
...커버 이미지를 보셨다시피, 새로운 UI가 [Spotify web](https://open.spotify.com) 버전이 아닌, 클라이언트에서도 적용시킬 수가 있습니다.

[Spicetify](https://github.com/khanhas/spicetify-cli) 같은 커스터마이징 툴을 안깔아도 돼고, 최신 버전이라면 애초에 이미 새로운 UI를 적용할 수 있는 방법이 있긴합니다;;

빠르게 설정방법으로 넘어가죠.

# 설정방법

1. 메모장, vscode같은 텍스트 파일 에디터 프로그램을 이용하여 prefs 파일을 엽니다.

   - 윈도우
   ```
   %appdata%\Spotify\prefs
   ```

   - 윈도우(마이크로소프트 스토어 버전)

   *...은 버전에 따라 달라집니다. 그러므로 `%localappdata%\Packages`폴더에서 먼저 찾아주셔야 합니다.*

   ```
   %localappdata%\Packages\SpotifyAB.SpotifyMusic_...\LocalState\Spotify\prefs
   ```

    ![윈도우 버전 스크린샷](https://nyan.shx.gg/O3s1bE.png)

   - 리눅스(snap으로 설치하지 않은 버전)
   ```
   ~/.config/spotify/prefs
   ```

   - 리눅스 (snap으로 설치한 버전)
   ```
   ~/snap/spotify/current/.config/spotify/prefs
   ```

2. pref 파일에 `ui.experience_override="xpui"`를 **추가**합니다.
   ![추가된 스크린샷](https://nyan.shx.gg/GRPrqz.png)

3. Spotify를 재시작합니다.

# 끝!

모두 설정이 끝났으면 재시작한 Spotify에서 해당 문구와 함께 새로운 UI가 적용이 됩니다.
![알림 스크린샷](https://nyan.shx.gg/fiCFwv.png)