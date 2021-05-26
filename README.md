
## 🏌️‍♂️ erwin을 사용하여 골프와 관련된 종합 정보를 제공하는 회사 ERD &amp; 정보시스템 구축


## 💡 어려웠던 부분들

1. 순환관계에서의 댓글와 게시판 구현 - **게시글 자체가 댓글이 되는 경우라서 x테이블을 따로 만드는 것이 아니라 일반형의 PK를 FK로 만들어서 순환 형태로 표현**

2. 출력항목세트를 별도의 메타정보로 관리한다. 문자타입 10개, 숫자타입 5개, 날짜타입 5개로 관리한다. - **Domains로 관리**

3. 본문은 별도의 테이블로 관리하며 text형식 외에도 다양한 형식이 올 수 있고 여러 개의 로우로 저장되기도 한다. 로우로 저장되는 데이터는 게시판에서 지정한 메타정보의 출력항목을 갖는다.

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
![image](https://user-images.githubusercontent.com/53335160/119692026-05f88400-be86-11eb-8125-bb6e9c44f565.png)

