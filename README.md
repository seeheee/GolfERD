
## 🏌️‍♂️ erwin을 사용하여 골프와 관련된 종합 정보를 제공하는 회사 ERD &amp; 정보시스템 구축

### 💡 어려웠던 부분들

1. 게시판 유형/ 글번호를 따로 테이블로 뺄지, 그냥 할지

2. 순환관계에서의 댓글와 게시판 구현 = (댓글/게시판 유무 확인 필드로 구현했는데 그게 맞는지)

3. 로우로 저장되는 데이터는 메타정보의 출력항목을 가진다.

4. 본문 테이블 따로 만들어서 로우 여러개랑 본문은 html등 여러 데이터 형식이 올 수 있다.

<br>

## 💡 생각해 보기 좋은 구축

### **1. 좋아요/싫어요 추천수 DB 설계**<br>
처음 게시판을 로딩할때 추천 테이블의 값을 count을 계속 해 올시 로딩이 오래걸린다.<br> 따라서 게시판(일반형) 테이블에 추천수, 반대수 컬럼을 따로 생성<br>
**회원번호(FK)와 게시글번호(FK)가 하나의 PK -> 하나의 게시글에는 회원 한면당 좋아요 혹은 싫어요 혹은 취소가 가능하기에 회원번호로 중복여부 확인**<br>
![image](https://user-images.githubusercontent.com/53335160/119469293-2ccd9200-bd82-11eb-8db3-eba8a59652fc.png)

### **2. 댓글과 대댓글의 계층구조 표현과 DB 설계**<br>
1️⃣ 댓글과 대댓글 테이블을 따로 구현할 경우<br>
![image](https://user-images.githubusercontent.com/53335160/119643290-88694f80-be56-11eb-9f72-030d8729ef21.png)

2️⃣ 댓글과 대댓글 테이블을 하나의 테이블로 구현할 경우ㅇ
이 경우에는 댓글의 깊이를 표시해 주어야 함<br>
예를 들어 댓글의 깊이는 0, 대댓글의 깊이는 1<br>

<br>

### 👀 5월 16일(1차 정보시스템 구축)

![image](https://user-images.githubusercontent.com/53335160/118454371-4132de80-b733-11eb-88b8-8d0049487f13.png)
![image](https://user-images.githubusercontent.com/53335160/118454484-61fb3400-b733-11eb-8455-6cf365f4eca4.png)
![image](https://user-images.githubusercontent.com/53335160/118454609-86efa700-b733-11eb-955d-83a70b138bb0.png)

<br>

### 👀 5월 20일(1차 ERD)
![image](https://user-images.githubusercontent.com/53335160/118842050-cff65580-b903-11eb-8cfb-eae6be7f2c7a.png)

<br>

### 👀 5월 26일(2차 ERD)
![image](https://user-images.githubusercontent.com/53335160/119643825-34129f80-be57-11eb-9e7a-a48f4a7a7791.png)![image](https://user-images.githubusercontent.com/53335160/119643901-47256f80-be57-11eb-9eaa-fd5a914ea692.png)
