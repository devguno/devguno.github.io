---
title: 윈도우 탐색기에서 SSH 서버 폴더 접근하기
author: guno
date: 2024-08-01 00:00:00 +0800
categories: [server]
tags: [server]
img_path:
---

## 윈도우 탐색기에 SSH 연결하는법

### 필요한 소프트웨어의 다운로드

1. sshfs-win 설치  [Install sshfs-win]
(https://github.com/winfsp/sshfs-win/releases/tag/v3.5.20357)

2. WinFsp 설치  [(]Install WinFsp]
(https://github.com/winfsp/winfsp/releases/tag/v2.0)

두가지 소프트웨어가 설치되면, 윈도우의 터미널을 엽니다.

명령어 입력: 다음 명령어를 입력하여 SSH 연결을 설정합니다. 

net use [드라이브 알파벳]: \\sshfs\\[아이디]@[주소]![포트]
(포트는 선택 사항입니다. 기본값은 22입니다.)
 

예를 들면 다음과 같습니다.
net use Y: \\sshfs\\user@111.11.111.11!22
명령어 입력 후, 설정한 드라이브가 탐색기에 표시됩니다.


이제 마치 로컬 드라이브처럼 SSH 서버의 파일을 관리할 수 있습니다


## 등록한 드라이브 삭제하기 (unmount)
net use [드라이브 알파벳]: \\sshfs\\[아이디]@[주소]![포트] /del

예시: net use \\sshfs\\user@111.11.111.11!22 /del
 

[nodejs]: https://nodejs.org/
[starter]: https://github.com/cotes2020/chirpy-starter
[pages-workflow-src]: https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site#publishing-with-a-custom-github-actions-workflow
[latest-tag]: https://github.com/cotes2020/jekyll-theme-chirpy/tags
