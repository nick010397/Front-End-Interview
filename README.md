# Front-End-Interview

# CS

## 1. 브라우저 주소창에 www.google.com을 입력하면 어떤 일이 일어날까요?

### A : 사용자가 웹 브라우저를 통해 google.com 을 입력하면 URL 주소 중 도메인 네임 부분을 DNS 서버에서 검색한다. DNS 서버에서 해당 도메인 네임에 해당하는 IP 주소를 찾아 사용자가 입력한 URL 정보와 함께 전달한다. 브라우저는 HTTP 프로토콜을 사용하여 요청 메시지를 생성하고 HTTP 요청 메시지는 TCP/IP 프로토콜을 사용하여 서버로 전송된다. 서버는 response 메시지를 생성하여 다시 브라우저에게 데이터를 전송한다. 브라우저는 response를 받아 파싱하여 화면에 렌더링한다.

### ```프로토콜```: 통신하기 위한 약속들을 기술적으로 잘 정의해 둔것이다.
### ```DNS(Domain Name System)```: 모든통신에는 주소가 필요하다. 출발지와 도착지의 주소를 알아야 통신을 할 수 있다. 우리는 이 주소를 IP라고 부른다. IP 주소로 변환하는 과정에 개입하는 것 <google.com의 IP 주소를 DNS 서버에 요청해 받아 왔고 요청 할 서버의 IP 주소를 알았으니>
### ```HTTP(HyperText Transfer Protocol)``` : 서버에 데이터를 요청하기 위해서는 HTTP 프로토콜이 필요하다.<작성한 HTTP요청 메시지는 TCP 프로토콜을 사용하여 인터넷을 거쳐 해당 IP 주소의 컴퓨터로 전송된다.>
### ```IP(Internet Protocol)```은 비신뢰성, 비연결지향 데이터그램 프로토콜로 패킷을 받아서 주소를 해석하고 경로를 결정하여 다음 호스트로 전송하는 역할을 한다.
### ```TCP(Transmissions Crontrol Protocol)```: 전송 제어 프로토콜로 데이터를 전송을 제어하고 데이터를 어떻게 보낼 지, 어떻게 맞출 지 정한다. <IP의 특징은 비신뢰성과 비연결성이다. 그래서 IP 프로토콜 만으로는 통신을 할 수 없다. 신뢰성과 연결성을 책임지기 위한 프로토콜이 TCP이다. 호스트와 호스트간의 데이터 전송은 IP(인터넷 계층 프로토콜)에 의지하면서 동시에 신뢰성 있는 전송에 대해서는 TCP가 책임지는 구조이다.>

<br><br>

## 2. Get 과 Post의 차이

### A: HTTP의 메소드로 둘 다 브라우저가 서버에 요청하는 것입니다. GET은 서버의 리소스에서 데이터를 요청할 때, POST는 서버의 리소스를 새로 생성하거나 업데이트할 때 사용한다.
- GET 요청은 캐시가 가능하다. 
- GET을 통해 서버에 리소스를 요청할 때 웹 캐시가 요청을 가로채 서버로부터 리소스를 다시 다운로드하는 대신 리소스의 복사본을 반환한다. HTTP 헤더에서 cache-control 헤더를 통해 캐시 옵션을 지정할 수 있다.
- GET 요청은 브라우저 히스토리에 남는다.
- GET 요청은 길이 제한이 있다.
- GET 요청은 중요한 정보를 다루면 안된다. (보안)
---
- POST 요청은 캐시되지 않는다.
- POST 요청은 브라우저 히스토리에 남지 않는다.
- POST 요청은 데이터 길이에 제한이 없다.

<br><br>

## 3. 객체지향프로그래밍(Object Oriented Programming)이란?

### A:컴퓨터 프로그래밍 패러다임 중 하나로, 프로그래밍에서 필요한 데이터를 추상화시켜 상태와 행위를 가진 객체를 만들고 그 객체들 간의 유기적인 상호작용을 통해 로직을 구성하는 프로그래밍 방법

- 장점

▶코드 재사용이 용이

남이 만든 클래스를 가져와서 이용할 수 있고 상속을 통해 확장해서 사용할 수 있다.

▶유지보수가 쉬움

절차 지향 프로그래밍에서는 코드를 수정해야할 때 일일이 찾아 수정해야하는 반면 객체 지향 프로그래밍에서는 수정해야 할 부분이 클래스 내부에 멤버 변수혹은 메서드로 존재하기 때문에 해당 부분만 수정하면 된다. 

▶대형 프로젝트에 적합

클래스 단위로 모듈화시켜서 개발할 수 있으므로 대형 프로젝트처럼 여러 명, 여러 회사에서 프로젝트를 개발할 때 업무 분담하기 쉽다.

- 단점

▶처리 속도가 상대적으로 느림

▶객체가 많으면 용량이 커질 수 있음

▶설계시 많은 시간과 노력이 필요

<BR><BR>

## 4. 프로세스와 스레드에 대해 설명해주세요

- Program : 어떤 작업을 위해 실행 할 수 있는 파일

### 프로세스(Process)란?

- ```"컴퓨터에서 연속적으로 실행되고 있는 컴퓨터 프로그램”```
- 메모리에 올라와 실행되고 있는 프로그램의 인스턴스(독립적인 개체)
- 운영체제로부터 시스템 자원을 할당받는 작업의 단위
- 즉, 동적인 개념으로는 실행된 프로그램을 의미한다.

### 특징
![image](https://user-images.githubusercontent.com/102947585/206659179-b2389e29-fe35-42e7-9976-f1960bce94c6.png)
-  프로세스는 각각 독립된 메모리 영역(Code, Data, Stack, Heap의 구조)을 할당받는다.
- 기본적으로 프로세스당 최소 1개의 스레드(메인 스레드)를 가지고 있다.


### 스레드(Thread)란?

- ```“프로세스 내에서 실행되는 여러 흐름의 단위”```
- 프로세스의 특정한 수행 경로
- 프로세스가 할당받은 자원을 이용하는 실행의 단위

### 특징
![image](https://user-images.githubusercontent.com/102947585/206662272-53d83b72-940e-4285-bbac-00cb43344793.png)

- 스레드는 프로세스 내에서 각각 Stack만 따로 할당받고 Code, Data, Heap 영역은 공유한다.
- 스레드는 한 프로세스 내에서 동작되는 여러 실행의 흐름으로, 프로세스 내의 주소 공간이나 자원들(힙 공간 등)을 같은 프로세스 내에 스레드끼리 공유하면서 실행된다.
- 같은 프로세스 안에 있는 여러 스레드들은 같은 힙 공간을 공유한다. 반면에 프로세스는 다른 프로세스의 메모리에 직접 접근할 수 없다.
- 각각의 스레드는 별도의 레지스터와 스택을 갖고 있지만, 힙 메모리는 서로 읽고 쓸 수 있다.
- 한 스레드가 프로세스 자원을 변경하면, 다른 이웃 스레드(sibling thread)도 그 변경 결과를 즉시 볼 수 있다.


## REST API에 대해 설명해주세요.
  
  ### A: REST API란 REST를 기반으로 만들어진 API를 의미합니다.
  
  ### REST란? 
  - REST(Representational State Transfer)의 약자로 자원을 이름으로 구분하여 해당 자원의 상태를 주고받는 모든 것을 의미합니다.
  - HTTP URI(Uniform Resource Identifier)를 통해 자원(Resource)을 명시하고,
  - HTTP Method(POST, GET, PUT, DELETE, PATCH 등)를 통해 <자원에 대한 행위>
  - 해당 자원(URI)에 대한 CRUD Operation을 적용하는 것을 의미합니다. <자원에 대한 행위의 내용 (Representations) >
  
  Create : 데이터 생성(POST)
  Read : 데이터 조회(GET)
  Update : 데이터 수정(PUT, PATCH)
  Delete : 데이터 삭제(DELETE)
  
  ### RESTful이란?
  RESTFUL이란 REST의 원리를 따르는 시스템을 의미합니다.   REST API의 설계 규칙을 올바르게 지킨 시스템을 RESTful하다 말할 수 있으며
  모든 CRUD 기능을 POST로 처리 하는 API 혹은 URI 규칙을 올바르게 지키지 않은 API는 REST API의 설계 규칙을 올바르게 지키지 못한 시스   템은 REST API를 사용하였지만 RESTful 하지 못한 시스템이라고 할 수 있습니다.


