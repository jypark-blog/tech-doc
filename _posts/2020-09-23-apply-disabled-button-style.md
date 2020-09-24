---
layout: post
title:  "Disabled Button에 Style 입히기"
date:   2020-09-23 23:49:00 +0900
categories: CSS
---

Disabled Button에 Style 적용
============================

눌려있는 상태 버튼을 사용하고 싶어서 [Bootstrap 눌림 버튼][bootstrap-button-toggle]을 사용 했습니다.  
해당 버튼을 사용하면서 disabled 속성을 추가했습니다.  
disabled 속성을 설정하면 모양만 보일뿐 제 기능을 못하게 됩니다.  
미처 생각하지 못한 부분은 disabled 속성을 주었을때 버튼이 눌려 있을때와 안눌려 있을때 구분을 못한다는 점이였습니다.  
이래저래 고생하다가 찾은 방법을 공유하고 싶어 포스트를 남기게 되었습니다.  
아래와 같이 [스타일 선택자][css-selector]를 사용하면 눌려있을때와 안눌려있을때는 구분하여 버튼에 스타일을 표현할 수 있습니다.  
`[attr*=value i]`에서 `*=`은 `value` 값이 속성에 존재하면 선택한다는 의미, `i`는 대소문자 구분을 안한다는 의미입니다.  

`before`
```
<button class="btn btn-primary" disabeld="disabeld" data-toggle="button" aria-pressed="true">눌림</button>
<button class="btn btn-primary" disabeld="disabeld" data-toggle="button" aria-pressed="false">안눌림</button>
```

`after`
```
<style>
    button:disabled[class*="btn-primary" i]
    {
        background-color: green;
    }
    button:disabled[class*="btn-light" i][class*="active" i]
    {
        background-color: red;
    }
</style>

<button class="btn btn-primary" disabeld="disabeld" data-toggle="button" aria-pressed="true">눌림</button>
<button class="btn btn-primary" disabeld="disabeld" data-toggle="button" aria-pressed="false">안눌림</button>
```

도움이 되었기를 바랍니다.

[bootstrap-button-toggle]: https://getbootstrap.com/docs/4.0/components/buttons/#toggle-states
[css-selector]: https://developer.mozilla.org/ko/docs/Web/CSS/Attribute_selectors