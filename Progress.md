11/18
main navbar v
map navbar(still working on) v
main page grid v
kakao map api v

11/19
- map navbar v
- login ui v -> 후에 position 옮기고 안에 정렬해야함
- login 기능 v

11/20
- signup ui -v
- 회원가입 기능 v
- 다크모드 v
-> map 에서도 sign out v
- my page 추가 v
- 회원정보 페이지 v
- 회원정보 수정 v

11/21
- 회원 탈퇴 완료 v
- 회원정보 페이지 완성 v
- 회원정보 수정 v
- 관리자 페이지 라우팅 v
- 관리자 로그인 시 관리자 페이지 보이게 하기 v
- working on :  관리자 페이지 머시기
- 관리자 페이지 - 회원 정보 관리 ui v
- navibar : 150%까지 안깨지게 수정

11/22
<관리자 페이지>
- 회원정보 관리 : sorting fcn V
- 회원정보 관리 : delete user V
- 게시글 관리 ui + sorting + search fcn 완료 v
- 게시글 관리 삭제 가능, list driven success. v
- board 게시판에 작성자 부분 직접 입력해야하는거 현재 로그인한 유저 자동 입력되게 수정 v
- 게시글 관리 : board 게시판 해당 글로 이동 가능
- 회원정보 관리: 이메일 누르면 mail 보낼 수 있게.. 보드에선 구현했는데 한번 백앤드 불러오면 해보기 [추가기능] 
- 회원 이름 클릭-> 작성 게시글 filter working on ..
-게시글 관리 ui + sorting + search fcn 완료 v
게시글 관리 삭제 가능, list driven success. v
-board 게시판에 작성자 부분 직접 입력해야하는거 현재 로그인한 유저 자동 입력되게 수정 v
- 게시글 관리 detail 완료: board 게시판 해당 글로 이동 가능
- 인기 게시글 : 조회수 순으로 정렬 완료
why at front ? : backend -> redundency . we are using list anyway..so if its better to use at front in my opinion
-유저 누르면 바로 이메일 보낼 수 있음 v [other?]
- active/inactive : 유저정보 저장.. 같은 이메일로 아이디 못만들게 함


세부적인 남은 기능
- 비밀번호 찾기 기능 : 반쯤 해놧는데 어디론가 가버림..ㅋㅋ
- 로그인 정보 틀리고 닫앗을 때, 에러가 유지되는점 -> clear 해줘야함 닫기버튼 누르면


11/23
문의하기 라우팅 완료
fab 만들어서 모든 페이지에서 floating 하고 hover 시 ask 띄움
누르면 문의 페이지로 이동
관리자탭에서는 문의 리스트 보고 질문자 누르면 답변할것 바이 이메일
로그인한 유저만 문의할 수 있게 수정
-문의하기 ui 완성
- 문의하기 cancle 시 이전 페이지로 돌아가기  : $router.go(-1)
-관리자페이지 문의 리스트 틀 반정도 잡음
- statistics page

Q&A DB
String no : auto increment
String userid
String subject
String email
String category (?)
String Date
bool status -> 답변 여부

필요한 기능
1. Select all : url - http://localhost:8080/user/admin/qna-management
2. View : url -http://localhost:8080/user/admin/qna-management/${no}
3. Update : 답변 여부 status -> false 를 true 로 바꾸기
4. insert : url - /qa/

currently 몇개 수정 완료쓰 (큐에이 카테고리 어케할지)
- 로그아웃/로그인할때 페이지 유지
- 졸졸 쫒아오는 문의하기 버튼 : 나중에 white theme에서 글자 색 바꾸는 방법 알아내야함 (minor)
- Q&A는 로그인한 유저만 가능 -> redirects
- Client : Q&A 누를시 문의 가능 (쿼리짜지면 문의를 insert랑 연결하면 됨)
- Admin: 
	인기게시글
	회원가입 상황은 일단 때려 박음(이건 나중에 시간이 나면 데이터랑 연결하기)
	신고 접수된 게시글 -> 나중에 시간나면 게시글에 신고 true false 넣으면 가능할듯. 필요한 기능이기도..?
	Q&A 관리 : 
		- no눌러서 내용 보기-> view page는 모달로 만들 예정
		- 모달창에서 이메일 눌러서 바로 답변할 수 있게
		- 답변 완료하면 답변 여부의 "답변"버튼 눌러서 완료 상태로 바꿀 것
		- 미답변만 보는 필터 추가할 예정
그렇게 하면 QA도 완료

