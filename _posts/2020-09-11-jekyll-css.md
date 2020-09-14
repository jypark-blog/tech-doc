---
layout: post
title:  "Jekyll CSS 적용"
date:   2020-09-11 16:25:00 +0900
categories: Jekyll
---

Jekyll 초기화 후 CSS 오류 수정
=============================

로컬에서는 화면이 제대로 나와 걱정없이 Github Page에 배포했습니다.  
하지만 Github Page에서 CSS가 적용안되고 화면이 깨져보였습니다.  
다음 내용을 참고하여 CSS 오류를 수정하였습니다. [적당주의][적당주의]  

아래 해석은 정확한 내용을 아니므로 참고만 바랍니다.  
baseUrl을 명시하지 않으면 `https://jypark-blog.github.io`를 base로 css 파일을 찾기 때문에 오류가 발생하고  
baseUrl을 명시하면 `https://jypark-blog.github.io/tech-doc`를 base로 css 파일을 찾기 떄문에 성공한다는 내용 같습니다.  

before  `_config.yml`
```
baseurl: ""
url: ""
```

after   `_config.yml`
```
baseurl: "/tech-doc"
url: "https://jypark-blog.github.io"
```

[적당주의]: https://lifetutorial.tistory.com/7