# index.jsp

<p>![index-jsp](https://user-images.githubusercontent.com/41488792/43357424-3ffb83c6-92bc-11e8-9722-3ea4549e7f3e.JPG)
<h6><script> 태그를 사용하여 jsp 문법을 쓰면 된다.<br>
location,href = “이동하고 싶은 jsp 파일”</h6></p>

# login.jsp
```jsp
  <%@ page language="java" contentType="text/html; charset=UTF-8"
    pageEncoding="UTF-8"%>
<!DOCTYPE html>
<html>
<head>
<meta http-equiv="Content-Type" content="text/html; charset=UTF-8">
<meta name="viewport" content="width=device-width", initial-scale="1">
<link rel="stylesheet" href="css/bootstrap.min.css">
<title>JSP 게시판 웹사이트</title>
</head>
<body>
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
	<script src="https://code.jquery.com/jquery-3.1.1.min.js"></script>
	<script src="js/bootstrap.js"></script> 
	

</body>
</html>
  ```
<h6> **width** 속성은 뷰포트의 크기를 조정한다. 특정한 숫자를 사용해 width=600이라고 할 수도 있고 devie-width와 같은 특정한 값을 사용할수 있는데, <strong>device-width</strong>는 100% 스케일에서 CSS 픽셀들로 계산된 화면의 폭을 의미한다.<br>
  **initial-scale** 속성은 페이지가 처음 로드될 때 줌 레벨을 조저한다.(사용자가 얼마나 페이지를 줌-인, 줌-아우트 할 수 있는지를 조정한다.</h6>

