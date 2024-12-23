# 게시판
## 게시판 생성
### method : post
### API endpoints : /boards

## 게시판 조회
### method : get
### API endpoints : /boards
### query String : pageNum (int page 번호)


## 게시판 수정
### method : put
### API endpoints : /boards/edit
### query String : editAt (String 수정시간)


## 게시판 삭제
### method : delete
### API endpoints : /boards 


# 게시글
## 게시글 생성
### method : post
### API endpoints : /posts
### query String : postAt (String 게시글 생성 시간)

## 게시글 조회
### method : get
### API endpoints : /posts/{id}

## 게시글 수정
### method : put
### API endpoints : /posts/edit/{id}
### query String : postEditAt(string 게시글 수정시간)

## 게시글 삭제
### method : delete
### API endpoint : posts/{id}


# 댓글
## 댓글 생성
### method : post
### API endpoints : /posts/{id}/comments
### query String : commentsPostAt(String 댓글 생성 시간)

## 댓글 조회
### method : get
### API endpoints : /posts/{id}/comments

## 댓글 수정
### method : put
### API endpoints : /posts/{id}/edit/comments
### query String : commentsEditAt (String 댓글 수정 시간)

## 댓글 삭제
### method : delete
### API endpoints : /posts/{id}/comments


# Entity
## Board Class
### private String boardName; (게시판 이름)
### private List<Post> post;

## Post Class
### private LocalDate postAt; (게시글 생성 시간) 
### private Long id; (게시글 id)
### private String postUserId; (작성자)
### private String title; (게시글 제목)
### private String contents; (본문 내용)
### private Comment comment; (댓글)

## Comment Class
### private LocalDate commentsAt; (댓글 생성 시간)
### private String commentUserId; (댓글 생성 유저 id)
### private String commentContents; (댓글 내용)

