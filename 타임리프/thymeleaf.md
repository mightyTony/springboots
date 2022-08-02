1. th:onclick = "" 안에서 location.href 로 동적 변수 받기
-----------------------------------------------------
ex : <button class="comment_deletebtn" th:onclick="|location.href='@{/comment/delete(user_code=${user.user_code},comment_code=${list.comment_code})}'|"></button>


2. th:text = ${} : div에 전달 받은 동적 변수 출력 
---------------------------------------------
ex : <div class="comment_nickname" th:text="${list.comment_nickname}"></div> 

3. img, th:src = ${}  : 이미지 소스 동적 경로 
-------------------------------------------
ex : <a> <img alt="프로필 사진" th:src="@{/image/profile/} + ${list.user_picture}"> </a>