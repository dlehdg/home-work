## 🕛 2주차 과제 반응형 웹 디자인



로그인 페이지 구현
<br><br>
자바스크립트를 사용해서  동적으로 클래스가 추가되는 상황등을 가정하여 구현



 <h2>✏사용된 기술</h2>

 <img alt="Html" src ="https://img.shields.io/badge/HTML5-E34F26.svg?&style=for-the-badge&logo=HTML5&logoColor=white"/> <img alt="Css" src ="https://img.shields.io/badge/CSS3-1572B6.svg?&style=for-the-badge&logo=CSS3&logoColor=white"/> 
<br>


## 디렉토리 구조

![image](https://github.com/dlehdg/home-work/assets/80308340/1e67ab7c-8c33-4cc3-b8c9-b1dbe6fbd476)



# 💻 구현 조건



## 1. 로그인 페이지 반응형 동작 (모바일)

<br>
화면 기준을 기준으로 반응형으로 구현

<br>
모바일 -> max-width : 600px <br>
태블릿, 데스크탑 -> min-width : 600px
<br><br>

![image](https://github.com/dlehdg/home-work/assets/80308340/2663b789-bd5e-45b1-bf9a-e866ed6fa069)

<br>

> 로그인과 관련된 부분을 감싼 요소를 통해서 그 요소를 통해 반응형 코드를 구성 <br>
> 기존에 버튼 요소들의 배치 위치를 변경

<br>


## 2. 이메일, 패스워드 입력 서식이 normal 상태일 경우

     #password, #email{
         background-color: transparent;
         width: 100%;
         border: none;
         box-shadow: none;
         border-bottom: 0.03125em solid #fff;
         outline: none;
         /* padding: 8px; */
         /* 선택적으로 테두리를 추가할 수 있습니다 */
         }

<br>

> 이메일과 패스워드의 입력 서식이 nomal인 상태일 때는 입력부분을 투명하게 하면서 border을 통해 밑줄을 표시하였다

<br><br>

## 3. 이메일, 패스워드 입력 서식이 valid 상태일 경우

![image](https://github.com/dlehdg/home-work/assets/80308340/950c5ed8-b634-4d55-bf7e-980090b70c5f)


<br>

> 입력 서식이 valid 상태가 되면 js를 통해 display를 none으로 지정한 이미지와 경고 문자를 불러오도록 실행

<br><br>

## 4. 이메일, 패스워드 입력 서식이 invalid 상태일 경우


![image](https://github.com/dlehdg/home-work/assets/80308340/2451e995-b27d-45a0-a1a2-7fe3243fc08c)

<br>

> 입력 서식이 invalid 상태인 경우 기존의 경고 문자와 이미지를 none 처리한뒤 invalid 이미지를 불러온다

<br><br>

## 5. 패스워드 입력 값이 visible 상태일 경우

![image](https://github.com/dlehdg/home-work/assets/80308340/4543c373-6369-4a54-95bc-b741a6401e77)

<br>

![image](https://github.com/dlehdg/home-work/assets/80308340/34f91657-a61a-4769-95a5-01be95e6bf5b)

<br>

> 패스워드 입력 값이 visible인 상태라면 경고 표시가 사라지고 그 자리에 체크마크가 들어오도록 구현

<br><br>

## 6. 입력 서식이 focus 상태일 경우
    


    


     #password:focus, #email:focus {
    border: 0.125em solid blue;
    border-bottom: 0.13125em solid #fff;

    }
    
<br>
    
> 입력 서식이 focus 상태일 때에는 입력서식 부분에 border을 통해 강조하였다

<br><br>


## markup

      <!DOCTYPE html>
      <html lang="ko">
      <head>
        <meta charset="UTF-8">
        <meta name="viewport" content="width=device-width, initial-scale=1.0">
        <title>EDIYA LOGIN</title>
        <link rel="stylesheet" href="./css/style.css">
      </head>
      <body>
        <div class="login-box">
          <!-- <img src="./image/coffee.svg" alt="" class="images"> -->
          <section class="login-text">
            <h2>로그인</h2>
      
            <p class="white-text">Welcome, Ediya Coffee</p>
            <p class="white-text-small">이디야커피에 오신 것을 환영합니다.</p>
          </section>
      
          
          
          <div class="login-wrap">
            <div class="email-box">
            
                <label for="email" class="input-text">이메일</label>
            
                <input type="email" name="email" id="email" required autofocus/>
                <img src="./image/error.png" alt="에러" class="error-image"/>
                <img src="./image/체크마크.svg" alt="에러" class="error-image checked"/>
                <span class="error-msg-email">이메일 입력 방법이 잘못되었습니다. (예: user@domain.io)</span>
                <!-- <div class="line"></div> -->
            
            </div>
            <!-- <div class="email">
              <label class="email-label " for="email" id="user-email">이메일</label>
              <input type="email" placeholder="yamoo9@euid.dev" required />
            </div> -->
            <div class="password-box">
              <label for="password" class="input-text">패스워드</label>
            
                <input type="password" name="password" id="password">
                <img src="./image/eye.png" alt="pw확인" class="eye-image"/>
                <img src="./image/eye-reverse.png" alt="pw체크" class="eye-image .reverse"/>
                <img src="./image/error.png" alt="에러" class="error-image"/>
                <span class="error-msg-pw">패스워드는 숫자, 영어 조합 6자 이상 입력해야 합니다</span>
                <!-- <div class="line"></div> -->
                <div class="check-box">
                  <input type="checkbox" name="check-boxs" id="email-checkbox" />
                  <label for = "email-checkbox" class="input-text-btn">이메일 저장</label>
                </div>
              </div>
            
            
            
            
            <section class="login-btn">
              <div class="login-btn-box">
              <button type="submit" class="white-btn">
                <p class="submit-text">로그인</p>
              </button>
              <img src="./image/화살표2.png" alt="화살표2" class="arrow-img"/>
            </div>
            <div class="login-btn-box">
              <button type="button" class="reverse-btn">
                <p class="reverse-text">회원가입 </p>
              </button>
              <img src="./image/화살표.svg" alt="화살표" class="arrow-img2"/>
            </div>
            </section>
          </div>
        </div>
      </body>
      </html>

  <br><br>

## test

  <br>

 ![image](https://github.com/dlehdg/home-work/assets/80308340/a9de00ed-f221-486e-8050-312e2470195a)

