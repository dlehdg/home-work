## 🕛 1주차

1주차 과제 제출

 <h2>✏사용된 기술</h2>

 Html, CSS

---

## 1-1. 전체 구조




mission-01 파일 안에 이미지와 css을 보관할 파일을 생성

이를 적용할 index.html 파일 생성

![image](https://github.com/dlehdg/home-work/assets/80308340/0bcc6849-0a74-4ca3-9739-0b6934beaa73)

[전체 구조]

---
<br>

## 1-2. HTML




html 요소는 클래스 이름이 boxA인 요소와 kamill 그리고 .gomgom 요소를 만들었다

그리고 이를 배치하기 위해 kamill과 gomgom을 center 클래스 이름의 div 요소에 묶었고

또한 boxA와 위에서 지정한 .center 요소를 중앙정렬 등 위치에 배치하기 위해 .main로 묶었다

<br>

![image](https://github.com/dlehdg/home-work/assets/80308340/55923a8d-762c-4b54-98bc-b2a2953ed640)



---
<br>

<br>


## 1-3. CSS

배경색 등의 파일등은 피그마에서 주어진 지정된 색 사용




<h3>배치</h3>
<br>




    .main {
      display: flex; 
      flex-direction: column;
      align-items: center;
     }



> display를 flex로 한뒤 중앙정렬과 함께 column 방향으로 배치

<br>



    .centers {
     display: flex;
     align-items: center;
     justify-content: center;
     }

> centers의 display를 flex로 하면서 수평으로 배치


---
<br>

<h3>버튼 hover 전</h3>

    .btn1 {
    position: absolute;
    width: 42px;
    height: 42px;
    flex-shrink: 0;
    fill:  rgba(0, 0, 0, 0.20);
    color: #ccc;
    margin-top: 20px;
    left: 0;
    bottom: 0;
    margin-bottom: 20px;
    margin-left: 20px;
     }


<br>

<h3>버튼 hover </h3>

    .btn1:hover{
      background: #0074E9;
      border: 0;
      z-index: 10;
      width: 100px;
      height: 42px;
      font-size: 15px;
      color: #fff;
  
    }

    .btn1:hover::before {
      content: "구매하기";
  
      padding-right: 10px;
    }



> 버튼에 hover시에 색 변경 및 befort를 통해 가상요소를 추가 하는 예제와 같은 스타일로 적용

<br>
<br>

---

## 1-4. TEST

![image](https://github.com/dlehdg/home-work/assets/80308340/745ae3e1-22db-4e4a-b83b-827da4f18820)
