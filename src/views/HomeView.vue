<!-- <template>
    <div class="common-layout">
      <el-container>
        <el-header>Header</el-header>
        <el-main>Main</el-main>
        <el-footer>Footer</el-footer>
      </el-container>
    </div>
  </template> -->

  
  <template>
    <div class="login-container">
      <div class="login-content">
        <h1 class="title">EducareBook</h1>
        <h2 class="subtitle">Login now</h2>
        <p class="welcome-message">Hi, Welcome back 👋</p>
        <button class="google-login">Login with Google</button>
        <div class="divider">
          <span>or Login with Email</span>
        </div>
        <form @submit.prevent="login" class="email-form">
          <input type="email" v-model="email" placeholder="Email" required>
          <input type="password" v-model="password" placeholder="Password" required>
          <div class="form-footer">
            <label class="remember-me">
              <input type="checkbox" v-model="remember"> Remember Me
            </label>
            <a href="#" class="forgot-password">Forgot Password?</a>
          </div>
          <button type="submit" class="login-button">Login</button>
        </form>
        <p class="sign-up-message">
          Not registered yet? <a href="#" class="sign-up-link">Create an account SignUp</a>
        </p>
      </div>
      <div class="login-illustration"></div>
    </div>
  </template>
  
  <script>
  export default {
    name: 'LoginView',
    data() {
      return {
        email: '',
        password: '',
        remember: false
      };
    },
    methods: {
      login() {
        // Implement your login logic here
        alert(`Login attempted with email: ${this.email}`);
      }
    }
  }
  </script>
  
  <style scoped>
  .login-container {
    display: flex;
    width: 100%;
    height: 100vh;
  }
  
  .login-content {
    padding: 40px;
    max-width: 480px;
    width: 100%;
    display: flex;
    flex-direction: column;
    justify-content: center;
    background-color: #fff;
  }
  
  .title {
    color: #E91E63;
    font-size: 2.5em;
    margin-bottom: 0.5em;
  }
  
  .subtitle {
    color: #333;
    font-size: 2em;
    margin-bottom: 0.25em;
  }
  
  .welcome-message {
    margin-bottom: 2em;
    color: #333;
  }
  
  .google-login {
    background-color: #db4437;
    color: white;
    padding: 10px 15px;
    border: none;
    border-radius: 4px;
    margin-bottom: 1em;
    cursor: pointer;
  }
  
  .divider {
    text-align: center;
    border-top: 1px solid #ccc;
    line-height: 0.1em;
    margin: 20px 0;
  }
  
  .divider span {
    background: #fff;
    padding: 0 10px;
  }
  
  .email-form input {
    width: 100%;
    padding: 10px;
    margin: 10px 0;
    border: 1px solid #ddd;
    border-radius: 4px;
  }
  
  .form-footer {
    display: flex;
    justify-content: space-between;
    align-items: center;
    margin-bottom: 20px;
  }
  
  .remember-me input {
    margin-right: 5px;
  }
  
  .forgot-password {
    color: #E91E63;
  }
  
  .login-button {
    background-color: #5c67f2;
    color: white;
    padding: 10px 15px;
    border: none;
    border-radius: 4px;
    cursor: pointer;
  }
  
  .login-button:hover {
    background-color: #4a52d4;
  }
  
  .sign-up-message {
    text-align: center;
    margin-top: 20px;
  }
  
  .sign-up-link {
    color: #E91E63;
  }
  
  .login-illustration {
    background: url('../assets/Picture1.png') no-repeat center center;
    background-size: cover;
    width: 50%;
  }

  /* Responsive styles if needed */
  @media (max-width: 768px) {
    .login-container {
      flex-direction: column;
      height: auto;
    }
  
    .login-illustration {
      width: 100%;
      height: 200px;
    }
  }
  </style>


<!--     
  <template>
    <div class="login-container">
      <div class="login-content">
        <header>
          <h1>EducareBook</h1>
          <button class="sign-up-btn">Sign Up</button>
        </header>
        <h2>Login now</h2>
        <p class="welcome-message">Hi, Welcome back 👋</p>
        <button class="google-login">Login with Google</button>
        <div class="divider">or Login with Email</div>
        <form @submit.prevent="login" class="email-form">
          <input type="email" v-model="email" placeholder="Email" required>
          <input type="password" v-model="password" placeholder="Password" required>
          <div class="form-options">
            <label class="remember-me">
              <input type="checkbox" v-model="remember"> Remember Me
            </label>
            <a href="#" class="forgot-password">Forgot Password?</a>
          </div>
          <button type="submit" class="login-button">Login</button>
        </form>
        <p class="sign-up-message">
          Not registered yet? <a href="#" class="sign-up-link">Create an account SignUp</a>
        </p>
      </div>
      <div class="login-illustration"></div>
    </div>
  </template>
  
  <script>
  export default {
    name: 'LoginView',
    data() {
      return {
        email: '',
        password: '',
        remember: false
      };
    },
    methods: {
      login() {
        // Implement your login logic here
        alert(`Login attempted with email: ${this.email}`);
      }
    }
  }
  </script>
  
  <style scoped>
  .login-container {
    display: flex;
    width: 100%;
    height: 100vh;
    background-color: #FBE0DC; /* Adjusted to match the pink background */
  }
  
  .login-content {
    padding: 40px;
    max-width: 480px;
    width: 100%;
    display: flex;
    flex-direction: column;
    justify-content: center;
    background-color: #fff; /* White background for the form area */
  }
  
  header {
    display: flex;
    justify-content: space-between;
    align-items: center;
  }
  
  .sign-up-btn {
    background: none;
    border: none;
    padding: 8px 20px;
    font-weight: bold;
    cursor: pointer;
    color: #333;
  }
  
  .title {
    color: #E91E63; /* Adjusted to match the pink title color */
    font-size: 2.5em;
    margin-bottom: 0.5em;
  }
  
  .subtitle {
    color: #333;
    font-size: 2em;
    margin-bottom: 0.25em;
  }
  
  .welcome-message {
    margin-bottom: 2em;
    color: #333;
  }
  
  .google-login {
    background-color: #EA4335; /* Google red color */
    color: white;
    padding: 10px 15px;
    border: none;
    border-radius: 4px;
    margin-bottom: 1em;
    cursor: pointer;
  }
  
  .divider {
    text-align: center;
    border-top: 1px solid #ccc;
    line-height: 0.1em;
    margin: 20px 0;
    color: #aaa;
  }
  
  .email-form input {
    width: 100%;
    padding: 10px;
    margin: 10px 0;
    border: 1px solid #ddd;
    border-radius: 4px;
  }
  
  .form-options {
    display: flex;
    justify-content: space-between;
    align-items: center;
    margin-bottom: 20px;
  }
  
  .remember-me input {
    margin-right: 5px;
  }
  
  .forgot-password {
    color: #EA4335; /* Matching the Google button color */
  }
  
  .login-button {
    background-color: #5c67f2;
    color: white;
    padding: 10px 15px;
    border: none;
    border-radius: 4px;
    cursor: pointer;
  }
  
  .login-button:hover {
    background-color: #4a52d4;
  }
  
  .sign-up-message {
    text-align: center;
    margin-top: 20px;
  }
  
  .sign-up-link {
    color: #E91E63; /* Pink color for the link */
  }
  
  .login-illustration {
    background-image: url('../assets/Picture1.png');
    background-size: cover;
    background-position: center;
    width: 50%;
  }
  
  @media (max-width: 768px) {
    .login-container {
      flex-direction: column;
      height: auto;
    }
  
    .login-illustration {
      width: 100%;
      height: 200px; /* Set a fixed height for mobile */
    }
  }
  </style>
   -->
