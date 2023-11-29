# Html-Projects
Food website
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Login</title>
    <link rel="stylesheet" href="/css/register.css">
    <link rel="shortcut icon" href="img/login favicon.png" type="image/x-icon">
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Montserrat:wght@300;400;500;600;700&display=swap');

*{
    margin: 8px;
    padding: 0;
    box-sizing: border-box;
    font-family: 'Montserrat', sans-serif;
    font-size:30px;
    text-align: center;
}
body{
    background-color: #c9d6ff;
    background: linear-gradient(to right, #e2e2e2, #c9d6ff);
    display: flex;
    align-items: center;
    justify-content: center;
    flex-direction: column;
    height: 100vh;
}
.register p{
    font-size: 14px;
    line-height: 20px;
    letter-spacing: 0.3px;
    margin: 20px 0;
}
.register{
    background-color: #fff;
    border-radius: 30px;
    box-shadow: 0 5px 15px rgba(0, 0, 0, 0.35);
    position: relative;
    overflow: hidden;
    width: 768px;
    max-width: 100%;
    min-height: 480px;
}
.register span{
    font-size: 12px;
}
.register button{
    background-color: #512da8;
    color: #fff;
    font-size: 12px;
    padding: 10px 45px;
    border: 1px solid transparent;
    border-radius: 8px;
    font-weight: 600;
    letter-spacing: 0.5px;
    text-transform: uppercase;
    margin-top: 10px;
    cursor: pointer;
}


.register button.hidden{
    background-color: transparent;
    border-color: #fff;
}

.register.active form{
    background-color: #fff;
    display: flex;
    align-items: center;
    justify-content: center;
    flex-direction: column;
    padding: 0 40px;
    height: 100%;
}

.register input{
    background-color: #eee;
    border: none;
    margin: 0px 0;
    padding: 15px 15px;
    font-size: 17px;
    border-radius: 10px;
    /* width: 0; */
    outline: none;
}

.form-register{
    position: absolute;
    top: 0;
    height: 100%;
    transition: all 0.6s ease-in-out;
}

.sign-in{
    left: 0;
    width: 50%;
    z-index: 2;
}

.register.active .sign-in{
    transform: translateX(100%);
}

.sign-up{
    left: 0;
    width: 50%;
    opacity: 0;
    z-index: 1;
}

.register.active .sign-up{
    transform: translateX(100%);
    opacity: 1;
    z-index: 5;
    animation: move 0.6s;
}
.register a{
    color: #333;
    font-size: 20px;
    text-decoration: none;
    margin: 15px 0 10px;
}
.register label{
    color: #333;
    font-size: 15px;
    text-decoration: none;
    margin: 15px  0px;
    
}
</style>
</head>



<body>
    <script>
        function validate() {
            
            alert("Server is not active!!")
        }
    </script>
    <div class="register">
        <b><header>Login</header></b>
        <form action="backend.php" name="myform" method="post" onsubmit="return validate()">
            <input class="input" type="email" name="name" placeholder="Enter your email"> </br> </br>
            <input class="input" type="password" name="password" placeholder="Enter your password"> </br></br>
            <input type="checkbox" name="checkbox" id="check1">
            <label for="check" class="text">Remember password</label> <br><br>
            <input type="submit" class="button" value="Login"> <br> <br>
            <b><a href="#">Forgot Password?</a></b> <br>
            <b><span class="text">Don't have an account?</b>
                <a href="register.html" class="text login-link">Signup</a> <br> <br>
        </form>
    </div>
</body>

</html>
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Registration</title>
    <link rel="stylesheet" href="/css/register.css">
    <link rel="shortcut icon" href="img/reg favicon.png" type="image/x-icon">
</head>

<body>
    <script>
        function validate() {
            var name = document.myform.name.value;
            // var email = document.myform.email.value;
            var password = document.myform.password.value;
            var cpassword = document.myform.cpassword.value;
            if (name == null || name == "") {
                alert("Name Can't Be Blank");
                return false;
            }
            else if (password.length < 6) {
                alert("Password Must Be Atleast 6 Digits")
                return false;
            }
            else if (password!=cpassword) {
                alert("Password and Confirm Password doesn't match!!")
                return false;
            }



            alert("Server is not active!!")
        }
    </script>

    <div class="register">
        <header>Signup</header>
        <form action="backend.php" name="myform" method="post" onsubmit="return validate()">
            <input class="input" type="text" name="name" placeholder="Enter your name"> <br> <br>
            <input class="input" type="email" name="email" placeholder="Enter your email"> <br> <br>
            <input class="input" type="number" name="number" placeholder="Enter your number"> <br><br>
            <input class="input" type="password" name="password" placeholder="Create a password"> <br> <br>
            <input class="input" type="password" name="cpassword" placeholder="Confirm a password"> <br> <br>
            <input type="checkbox" name="checkbox" id="check">
            <b><label for="check" class="text">I agree to all <a href="TnC.html">terms and conditions</a> </label></b> <br><br>
            <input type="submit" class="button" value="Signup"> <br> <br>
            <b><span class="text">Already have an account?</b>
                <a href="login.html" class="text login-link">Login</a>
        </form>
    </div>
</body>

</html>
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Terms & Conditions</title>
    <link rel="shortcut icon" href="img/t&c favicon.png" type="image/x-icon">
    <style>
        * {
            padding: 0;
            margin: 0;
            width: 100%;
            box-sizing: border-box;
        }

        h2 {
            padding: 20px;
        }

        .text {
            padding-left: 25px;
            font-style: italic;
            font-size: 20px;
            padding-right: 25px;
        }
    </style>
</head>

<body>
  

        
        <div>
            <img height="500px" src="/img/privacy.jpg" alt="">
            <h2>Terms and Conditions</h2>
            <div class="text">
                <p>
                    This Website is committed to protecting and respecting your privacy.
                    This policy together with our terms of use and any other documents referred to here set out the core
                    principle on which any personal data we collect from you or that you provide to us, will be
                    processed by us.
                    Please read the following carefully to understand our views and practices regarding your personal
                    data and how we will treat it.
                    We keep certain basic information when you visit our website and recognize the importance of keeping
                    that information secure and letting you know what we will do with it.
                    This policy only applies to our website. If you leave our website via a link or otherwise, you will
                    be subject to the policy of that website provider. We have no control over the policy or terms of
                    other websites. It is your responsibility to check their policy before continuing to access them.
                </p>
            </div>
            <br>
            <h2>Information we may collect from you</h2>
            <div class="text">
                <pre><p>
We may collect and process the following information about you:
  - Information that you provide by filling in forms on our site.
  - Information provided at the time of registering as a user on our website subscribing to our services or 
    requesting further assistance
  - Information you provide when reporting an issue with our website
  - When you contact us, a record of that correspondence
  - Completed surveys that we use for research purposes; although you do not have to respond to them.
                    </p></pre>
            </div>
            <br>
            <h2>IP Address and Cookies</h2>
            <div class="text">
                <p>
                    We may collect information about your computer, including where available, your IP address,
                    operating system, and browser type. We also collect data for system administration and to report
                    aggregate information to our advertisers.
                    This is statistical data about our users browsing actions and patterns, and does not identify any
                    individual or collect personal information to our third-party advertisers.
                    You may refuse to accept cookies by activating the setting on your browser which allows you to
                    refuse cookies. However, if you select this setting you may be unable to access certain parts of our
                    website. Unless you have adjusted your browser setting so that it will refuse cookies, our system
                    will issue cookies when you log on to our website.
                </p>
            </div>
            <br>
            <h2>Where we store your personal data</h2>
            <div class="text">
                <p>
                    All information you provide to us is stored on our secure servers. Any payment transactions will be
                    encrypted. Where we have given you (or where you have chosen) a password which enables you to access
                    certain parts of our site, you are responsible for keeping this password confidential. We ask you
                    not to share the password with anyone.
                </p>
            </div>
            <br>
            <h2>Your Rights</h2>
            <div class="text">
                <p>
                    You have the right to ask us not to process your personal data for marketing purposes. We will
                    usually inform you (before collecting your data) if we intend to use your data for such purposes or
                    if we intend to disclose your information to any third party for such purposes. You can exercise
                    your right to prevent such processing by checking certain boxes on the forms we use to collect your
                    data. You can also exercise the right at any time by contacting us via email. Our website may, from
                    time to time, contain links to and from the websites of our partner networks, advertisers, and
                    affiliates. If you follow a link to any of these websites, please note that these websites have
                    their own privacy policies and that we do not accept any responsibility or liability for these
                    policies. Please check these policies before you submit any personal data to these websites.
                </p>
            </div>
        </div>
    

</body>

</html>
