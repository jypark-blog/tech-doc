---
layout: post
title:  "Credential Issue"
date:   2020-09-11 16:10:00 +0900
categories: Git
---

Git 프로젝트별 자격 증명
=======================


Visual Studio Code로 Jekyll 프로젝트 생성 후 [Github][Github]에 동기화를 시도했습니다.

그러나 Push를 하면 403 에러가 발생했습니다.  
403 응답은 권한 에러로 로컬 git에 설정된 계정이 Github에 접근할 수 없다는 말이였습니다.  
기존에 다른 게정으로 Github에 업로드를 하였고 그 계정으로 Push를 시도하고 있었습니다.  
프로젝트마다 git 계정 설정을 찾던중 아래 명령어를 알게 되었지만 해결되지 않았습니다.  

```
git config user.name 'username'
git config user.email 'useremail'
```

~~제어판에서 `자격 증명 관리자`를 검색하고 `https://github.com`항목을 모두 삭제한 후  
다시 push를 하니 자격 증명을 물어보는 창이 나왔습니다.~~

3일뒤 다시 실행하니 같은 증상이 반복하여 찾는 중입니다...

[Github]: https://github.com/