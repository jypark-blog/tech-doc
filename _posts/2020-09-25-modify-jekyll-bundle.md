---
layout: post
title:  "Jekyll 로컬 PC 실행 오류"
date:   2020-09-25 00:12:00 +0900
categories: Jekyll
---

Jekyll 로컬에서 실행
===================

집에서 jekyll을 설치하고 로컬로 실행 했지만 오류가 발생했습니다.  
`jekyll serve Traceback (most recent call last):`...  
`jekyll serve`를 했을때 나오는 오류 내역을 구글에 검색해 보니 [Jekyll 문제 수정][jekyll-ref]을 찾을 수 있었습니다.  
원인은 코드를 다른 PC 환경에서 만들고 github에 올린뒤 집에서 다시 받아서 사용을 할 때  
다른 PC 환경의 ruby bundle 버전과 집 ruby bundle이 맞지 않아서 발생한 오류였습니다.  
전 위 참조 주소에서 `gem.lock`을 삭제하고 다시 설치 하는 방법으로 문제를 해결했습니다.  

감사합니다.  


[jekyll-ref]: https://thecodinglog.github.io/ruby/2019/02/28/jekyll-trouble-shooting.html
