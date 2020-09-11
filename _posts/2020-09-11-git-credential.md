---
layout: post
title:  "Credential Issue"
date:   2020-09-11 16:10:00 +0900
categories: Git
---

Visual Studio Code 에디터를 사용하여 Jekyll로 프로젝트 생성 후 Github에 push를 해야됐습니다.
그래야 github page에 배포가 되고 화면이 보입니다.

근데 아무리 Push를 해도 403에러가 났습니다.
기존에 다른 게정으로 연결 해놨는데 그 계정으로 업로드가 되었습니다.

그래서 프로젝트마다 계정 설정을 찾던 도중 아래 명령어를 알게 되었지만 같은 증상이 나타났습니다.

```
git config user.name
git config user.email
```

제어판에 `자격 증명`을 입력하고 `https://github.com` 항목을 모두 지우고 다시 push를 하니 자격 증명을 물어보는 창이 나왔습니다.
드디어 로그인을 하고 푸쉬를 한 결과입니다.

지금 Jekyll로 만들어진 css가 적용이 안되어 알아보러 가야겠습니다.