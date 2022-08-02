1. th:onclick = "" 안에서 location.href 로 동적 변수 받기
-----------------------------------------------------
ex : th:onclick="|location.href='@{/comment/delete(user_code=${user.user_code},comment_code=${list.comment_code})}'|">


2. th:text = ${} : 전달 받은 동적 변수 출력 
---------------------------------------------
ex : th:text="${list.comment_nickname}"

3. img, th:src = ${}  : 이미지 소스 동적 경로 
-------------------------------------------
ex : th:src="@{/image/profile/} + ${list.user_picture}">