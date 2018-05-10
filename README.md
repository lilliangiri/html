# html
<html>
<head>
<title>Registration</title>
<script type="text/javascript">
function validateall()
{
var flag=false;
if(validateName())
{
if(validatepassword())
{
if(validateemail())
{
if(validatephno())
{
flag=true;
}
}
}
}
return flag;
}
function validateName()
{
var x=document.myform.sname.value;
if(x==null||x=='')
{
alert("Please enter Name");
return false;
}
if(x.length<6)
{
alert("Name should contain atleast 6 characters");
return false;
}
var namepattern=/[a-z]/i;
if(!namepattern.test(x))
{
alert("enter valid name that contains only characters");
return false;
}
return true;
}
function validatepassword()
{
var x=document.myform.password.value;
if(x==null||x=='')
{
alert("Please enter the Password");
return false;
}
if(x.length<6)
{
alert("Password should contain atleast 6 characters");
return false;
}
return true;
}


function validateemail()
{
var x=document.myform.email.value;
var emailpattern=/^[a-zA-Z][a-zA-Z0-9_.]*@[a-zA-Z][a-zA-Z0-9]*.[a-zA-Z][a-zA-Z0-9]{3}$||^[a-zA-Z][a-zA-Z0-9_.]*@[a-zA-Z][a-zA-Z0-9]*.[a-zA-Z][a-zA-Z0-9]{2}.[a-zA-Z][a-zA-Z0-9]{2}$/;
if(x==null||x=='')
{
alert("Please enter the Email");
return false;
}
if(x.length<6)
{
alert("email address should not contain less than 6 characters ");
return false;
}
if(!emailpattern.test(x))
{
alert("Enter valid email address");
return false;
}
return true;
}
function validatephno()
{
var x=document.myform.phno.value;
var phnopattern=/[0-9]/;
if(x==null||x=='')
{
alert("Please enter the Phone number");
return false;
}

if(x.length>10)
{
alert("phone number must contain 10 digits ");
return false;
}
if(x.length<10)
{
alert("phone number must contain 10 digits ");
return false;
}
if(!phnopattern.test(x))
{
alert("enter valid phone number");
return false;
}
return true;
}
</script>
</head>
<body bgcolor="lightgreen">
<form name="myform" onsubmit="return validateall();" method="post" action="insert.php">
<table border="0" align="center">
<tr>
<td>Name: </td>
<td><input type="text" name="sname" size="25" maxlength="35" ></td>
</tr>
<tr>
<td>Password: </td>
<td><input type="password" name="password" size="25" maxlength="15" ></td>
</tr>
<tr>
<td>E-mail id: </td>
<td><input type="text" name="email" size="25" maxlength="35"></td>
</tr>
<tr>
<td>phone number: </td>
<td><input type="text" name="phno" size="25" maxlength="12"></td>
</tr>
<tr><td><input type="submit" value="submit" name="ten" ></td>
<td><input type="reset" value="Reset" name="eleven"></td>
</tr>
 </table>
  </form>
</body>
</html>

