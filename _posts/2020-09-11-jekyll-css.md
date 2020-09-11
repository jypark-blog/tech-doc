---
layout: post
title:  "Jekyll CSS 적용"
date:   2020-09-11 16:25:00 +0900
categories: Jekyll
---

처음 페이지를 배포했는데 CSS가 적용이 안되어 화면이 깨져보였습니다.

아래 주소를 참고하여 CSS를 적용하였습니다. https://lifetutorial.tistory.com/7

before
```
baseurl: "" # the subpath of your site, e.g. /blog
url: "" # the base hostname & protocol for your site, e.g. http://example.com
```

after
```
baseurl: "/tech-doc" # the subpath of your site, e.g. /blog
url: "https://jypark-blog.github.io" # the base hostname & protocol for your site, e.g. http://example.com
```