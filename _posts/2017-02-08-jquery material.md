---
title:  "jQuery"
published: true
permalink: jquery.html
summary: "jQuery material"
tags: [news, getting_started]
---

## jQuery

jQuery는 DOM 준비가 완료 될 때 실행 할 함수를 첨부하는 몇 가지 방법을 제공한다.

### 1. $(function(){ ... })

### 2. $(document).ready(function(){ ... })

### 3. $("document").ready(function(){ ... })

### 4. $("img").ready(function((){ ... })
	
### 5. $().ready(function(){ ... })

```
jQuery 3.0부터는 **$(function(){ ... })** 구문 만 권장합니다.
다른 구문도 작동은 하지만 사용되지는 않습니다.
이는 선택 항목이 .ready()메서드의 동작에 영향을 미치지 않아 비효율적 메서드의 동작에 대한 가정을 초래할 수 있기 때문입니다.
예를 들어 $("document").ready(function(){ ... }) 구문은 아무것도 선택하지 않은 "document"와 함께 작동합니다.
$("img").ready(function(){ ... }) 구문은 문서가 준비 될 때까지 대기하지만 이미지가 준비 될 때까지 기다립니다.

<script>
	$(function(){
		alert("스크립트 쉽죠잉~~");
	});
</script>

```

{% include links.html %}