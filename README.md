# index.jsp

<p>![index-jsp](https://user-images.githubusercontent.com/41488792/43357424-3ffb83c6-92bc-11e8-9722-3ea4549e7f3e.JPG)
<h6><script> 태그를 사용하여 jsp 문법을 쓰면 된다.<br>
location,href = “이동하고 싶은 jsp 파일”</h6></p>

# login.jsp
```jsp
  
<meta http-equiv="Content-Type" content="text/html; charset=UTF-8">
<meta name="viewport" content="width=device-width", initial-scale="1">
<link rel="stylesheet" href="css/bootstrap.min.css">
<title>JSP 게시판 웹사이트</title>

  ```
 반응형 웹에 사용되는 meta 태그를 넣어주자 (bootstrap 사용)<br>
 **width** 속성은 뷰포트의 크기를 조정한다. 특정한 숫자를 사용해 width=600이라고 할 수도 있고 devie-width와 같은 특정한 값을 사용할수 있는데, <strong>device-width</strong>는 100% 스케일에서 CSS 픽셀들로 계산된 화면의 폭을 의미한다.<br>
  **initial-scale** 속성은 페이지가 처음 로드될 때 줌 레벨을 조저한다.(사용자가 얼마나 페이지를 줌-인, 줌-아우트 할 수 있는지를 조정한다.<br>
 **rel="stylesheet"** 스타일 시트는 html이 가지는 불편함 점을 해소하기 위해서 만들어진 html의 보완 도구다.(CSS사용)<br>
 ```jsp
 <nav class="navbar navbar-default">
		<div class="navbar-header">
			<button type="button" class="navbar-toggle collapsed"
				data-toggle="collapse" data-target="#bs-example-navbar-collapse-1"
				aria-expanded="false">
				<span class="icon-bar"></span>
				<span class="icon-bar"></span>
				<span class="icon-bar"></span>
			</button>
			<a class="navbar-brand" href="main.jsp">JSP 게시판 웹 사이트</a>
		</div>
		<div class="collapse navbar-collapse" id="bs-example-navbar-collapse-1">
			<ul class="nav navbar-nav">
				<li><a href="main.jsp">메인</a></li>
				<li><a href="bbs.jsp">게시판</a></li>
					
			</ul>
			<ul class="nav navbar-nav navbar-right">
        		 <li class="dropdown">
         		  <a href="#" class="dropdown-toggle" 
          			  data-toggle="dropdown" role="button" aria-haspopup="true" 
           			  aria-expanded="false">접속하기 <span class="caret"></span></a>
      		<ul class="dropdown-menu">
      		        <li class="active"><a href="login.jsp">로그인</a></li>
             		<li><a href="join.jsp">회원가입</a></li>
            </ul>    
         		</li>
       		</ul>

		</div>
	</nav>
  ```
 nav 태그는 사이트에서 주요한 네비게이션 역할을 하는 링크 그룹을 담을 때 사용합니다. nav 요소를 사용하면, 스크린 리더를 이용하는 사용자가 네비게이션을 쉽고 빠르게 찾을 수 있고, 필요하지 않을 경우 건너뛰기 할 수 있습니다.<br>
**숨김기능 구현**(CSS js )<br>
태그에 **data-toggle="collapse"**와  **data-target**을 붙이기만 하면 숨김 가능한 다른 태그를 제어하게 된다. data-target 속성은 숨김을 적용할 css 선택자를 값으로 받는다. 숨김 가능한 태그에 collapse 클래스를 잊지 마라. <br>
**droptdwon 사용하기**(bootstrap)<br>
a 태그를 사용할 때에 href="#"을 넣으므로써 현재 가르키는 링크가 없다는 것을 알려주고<br>
**data-toggle="dropdwon"** 속성을 사용하여 dropdown을 구현한다. aria-haspopup -> 텍스트 필드와 연관된 하위 수준의 메뉴가 있으면 true, 그렇지 않으면 false, aria-expanded 펼침 상태 <br><br>
class ="active" 하면 현재 선택이 되었다는 뜻(현재 선택된 홈페이지를 의미) 위의 코드에 따르면 login.jsp가 현재 선택된 홈페이지라는 것을 표시해준다.(파란색으로 표시됨)<br>
```jsp
<div class="container">
		<div class="col-lg-4"></div>
		<div class="col-lg-4">
			<div class="jumbotron" style="padding-top: 20px;">
				<form method="post" action="loginAction.jsp">
					<h3 style="text-align: center;">로그인 화면</h3>
					<div class="form-group">
						<input type="text" class="form-control" placeholder="아이디" name="userID" maxlength="20">
					</div>
					<div class="form-group">
						<input type="password" class="form-control" placeholder="비밀번호" name="userPassword" maxlength="20">
					</div>
					<input type="submit" class="btn btn-primary form-control" value="로그인">
				</form>
			</div>
		</div>
		<div class="col-lg-4"></div>
	</div>
```
**콘테이너**
>부트스트랩은 사이트 콘텐츠를 감싸고 그리드 시스템을 만들 콘테이너가 필요함<br>
1.반은형 고정폭 콘테이너= .container<br>
2.뷰포트 전페폭까지 늘어나는 최대폭 콘테이너= .container-fluid<br>
class="container"를 사용해 component를 감싸줄 container를 만든다.<br>
jumbotron 템플릿 꾸며주기<br>


**form 태그**(html)<br>
>속성<br>
<li>action : 폼을 전송할 서버 쪽 스크립트 파일을 지정합니다.</li>
<li>name : 폼을 식별하기 위한 이름을 지정합니다.</li>
<li>accept-charset : 폼 전송에 사용할 문자 인코딩을 지정합니다.</li>
<li>target : action에서 지정한 스크립트 파일을 현재 창이 아닌 다른 위치에 열도록 지정합니다.</li>
<li>method : 폼을 서버에 전송할 http 메소드를 정합니다. (GET 또는 POST)</li>
form 사용법 : http://the3.tistory.com/53 <br>
submit을 통해 action="loginAction.jsp"로 <br>

**주의점:** form-group와 input 그룹은 같이 쓰면 안된다. form-group안에 input을 
 
 

