<template>
	<div class="bg">
		<div class="register">
			<form>
				<h2 style="color:white; margin-bottom:20px;">Sign Up</h2>
          <div class="form-group wrap-input2">
            <input
              type="text"
              class=" input2 "
              v-model="name"
              placeholder="Username"
              required="required"
            >
          </div>

          <div class="form-group wrap-input2">
            <input
              type="text"
              class=" input2 "
              v-model="contact"
              placeholder="Contact no"
              required="required"
            >
          </div>
          <div class="form-group wrap-input2">
            <input
              type="email"
              class=" input2 "
              v-model="email"
              placeholder="E-mail"
              required="required"
            >
          </div>
          <div class="form-group wrap-input2">
            <input
              type="password"
              class="input2"
              v-model="password"
              placeholder="Password"
              required="required"
            >
          </div>
           <div class="form-group">
            <button type="submit" class="btn btn-success col-lg-12" @click="storedata">
              Sign Up
            </button>
            <!-- <a href="#" class="fp">Forgot Password?</a> -->
          </div>
          <div class="text-light t1">
          	<label>
          	<p>Have an account?
          		<router-link to="/" style="color:white;" class="space"> Login here</router-link></p>
            </label>
          </div>
			</form>
		</div>
	</div>
</template>
<script>
export default {
  data() {
    return {
      name: "",
      contact: "",
      email: "",
      password: ""
    };
  },
  methods: {
    storedata() {
      if (
        this.name != "" &&
        this.contact != "" &&
        this.email != "" &&
        this.password != ""
      ) {
        localStorage.setItem("name", this.name);
        localStorage.setItem("email", this.email);
        localStorage.setItem("contact", this.contact);
        localStorage.setItem("password", this.password);
        console.log("deveshi");
        this.$router.push("/");
      } else {
        window.alert("Required Valid Details");
      }
    }
  }
};
</script>
<style scoped>
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
	.register{
		position: absolute;
		top :10%;
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
.space{
	margin-left: 15px;
}
.t1{
	font-size: 18px;
}

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
		left :10%;
		width: 300px;

	}
}
</style>
