//댓글 저장 No Ajax
```java
	@PostMapping("/comment")
	public RedirectView InsertComment(@RequestParam("user_code") int user_code,
									  @RequestParam("comment_text") String comment_text,
									  @RequestParam("writer_code") int writer_code,
									  @RequestParam("user_id") String user_id) throws Exception {
		System.out.println("인서트 테스트");
		ProFileVO pVo = new ProFileVO();
		pVo.setUser_code(user_code);
		pVo.setComment_context(comment_text);
		pVo.setWriter_code(writer_code);
		stimProfileService.InsertComment(pVo);
		
		String url = "/profile/" + user_code;
		System.out.println(url);
		
		return new RedirectView(url);
	}
```