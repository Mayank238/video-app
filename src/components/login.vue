<template>
	<div class="bg">
		<div class="login">
		  <form>
        <h2 style="color:white;">Log in</h2>
          <div class="form-group wrap-input2">
            <input
              type="text"
              class=" input2 "
              placeholder="Username"
              required="required"
            >
          </div>
          <div class="form-group wrap-input2">
            <input
              type="password"
              class="input2"
              placeholder="Password"
              required="required"
            >
          </div>
          <div class="form-group">
            <button type="submit" class="btn btn-success col-lg-5">Log in</button>
            <!-- <a href="#" class="fp">Forgot Password?</a> -->
          </div>
          <div >
            <label style="color:gray;">
              <input type="checkbox" > Remember me
            </label>
          </div>
          <div class="form-group">
            <a href="#" class="fp" style="color:white;">Forgot Password?</a>
          </div>
      </form>
        <p class>
        <a href="#" style="color:white;">Create an Account</a>
        </p>
    </div>
	</div>
</template>
<style>


.bg {
  /* The image used */
  background-image: url('https://backgroundcheckall.com/wp-content/uploads/2017/12/web-development-background-8.jpg');

  height: 100vh;

  /* Center and scale the image nicely */
  background-position: center;
  background-repeat: no-repeat;
  background-size: cover;
  background-attachment: fixed;
	}

	.login {
		position: absolute;
		top :20%;
		left :40%;
	}
	.wrap-input2 {
  border-bottom: 1px solid #adadad;
  margin-bottom: 37px;
}

.input2 {
    background: none;
    border:none;
    outline: none;
    display: flex;
    font-family: Poppins-Regular;
    font-size: 20px;
    color: white;
}

./*fp{
  color: white;
}*/

.col-1 {width: 8.33%;}
.col-2 {width: 16.66%;}
.col-3 {width: 25%;}
.col-4 {width: 33.33%;}
.col-5 {width: 41.66%;}
.col-6 {width: 50%;}
.col-7 {width: 58.33%;}
.col-8 {width: 66.66%;}
.col-9 {width: 75%;}
.col-10 {width: 83.33%;}
.col-11 {width: 91.66%;}
.col-12 {width: 100%;}

@media only screen and (max-width: 768px) {
  /* For mobile phones: */
  /*[class*="col-"] {
    width: 100%;
  }*/
  .bg{
  	background-position: center;
  }
  .login {
		position: absolute;
		top :25%;
		left :15%;
		width: 300px;

	}
}
</style>

<!-- https://backgroundcheckall.com/wp-content/uploads/2017/12/web-development-background-8.jpg -->
