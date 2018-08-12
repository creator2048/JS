<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Title</title>
    <script>
        function showTips(spanID,msg) {
            var span = document.getElementById(spanID);
            span.innerHTML = msg;
        }
        function checkUsername() {
            var uValue = document.getElementById("username").value;
//          alert(uValue);
            var span = document.getElementById("span_username");
            if (uValue.length < 6){
                span.innerHTML = "抱歉，太短了。"
            }else{
                span.innerHTML = "可以了。"
            }
        }
        function checkForm() {
            var flag = checkUsername();
            return flag;
        }
    </script>
</head>
<body>
    <form action="../images/03.jpg" onsubmit="return checkForm()">
        用户名：<input type="text" id="username" onblur="checkUsername()" onfocus="showTips('span_username','用户名不得少于六位')" onkeyup="checkUsername()"/><span id="span_username"></span><br/>
        <input type="submit" value="注册">
    </form>
</body>
</html>
