
## 🏌️‍♂️ erwin을 사용하여 골프와 관련된 종합 정보를 제공하는 회사 ERD &amp; 정보시스템 구축

### 💡 어려웠던 부분들

1. 게시판 유형/ 글번호를 따로 테이블로 뺄지, 그냥 할지

2. 순환관계에서의 댓글와 게시판 구현 = (댓글/게시판 유무 확인 필드로 구현했는데 그게 맞는지)

3. 로우로 저장되는 데이터는 메타정보의 출력항목을 가진다.

4. 본문 테이블 따로 만들어서 로우 여러개랑 본문은 html등 여러 데이터 형식이 올 수 있다.

### 💡 생각해 보기 좋은 구축

1. 좋아요/싫어요 추천수 count와 db 설계

2. 댓글과 대댓글의 계층구조 표현 / db 설계


### 👀 5월 16일(1차 정보시스템 구축)

![image](https://user-images.githubusercontent.com/53335160/118454371-4132de80-b733-11eb-88b8-8d0049487f13.png)
![image](https://user-images.githubusercontent.com/53335160/118454484-61fb3400-b733-11eb-8455-6cf365f4eca4.png)
![image](https://user-images.githubusercontent.com/53335160/118454609-86efa700-b733-11eb-955d-83a70b138bb0.png)


