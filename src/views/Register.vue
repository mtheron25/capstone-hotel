<template>
  <div id="main-wrapper" class="container">
    <div class="row justify-content-center">
      <div class="col-xl-10">
        <div class="card border-0">
          <div class="card-body p-0">
            <div class="row no-gutters">
              <div class="col-lg-6">
                <div class="p-5">
                  <div class="mb-5">
                    <h3 class="h4 font-weight-bold text-theme">Sign Up</h3>
                  </div>

                  <h6 class="h5 mb-0">Hello there!</h6>
                  <p class="text-muted mt-2 mb-5">
                    Enter your details to start exploring our famous suites.
                  </p>

                  <form @submit.prevent="login" class="form">
                    <div class="form-group">
                      <label for="exampleInputName1">Full Names</label>
                      <input
                        type="name"
                        class="form-control"
                        id="exampleInputName1"
                      />
                    </div>
                    <div class="form-group">
                      <label for="exampleInputEmail1">Email address</label>
                      <input
                        type="email"
                        class="form-control"
                        id="exampleInputEmail1"
                      />
                    </div>
                    <div class="form-group">
                      <label for="exampleInputContact1">Contact</label>
                      <input
                        type="number"
                        class="form-control"
                        id="exampleInputContact1"
                      />
                    </div>
                    <div class="form-group mb-5">
                      <label for="exampleInputPassword1">Password</label>
                      <input
                        type="password"
                        class="form-control"
                        id="exampleInputPassword1"
                      />
                    </div>
                    <button type="submit" class="btn btn-theme">
                      Register
                    </button>
                  </form>
                </div>
              </div>

              <div class="col-lg-6 d-none d-lg-inline-block">
                <div class="account-block rounded-right">
                  <img
                    src="https://i.ibb.co/L0r5h7W/ootp-beach-1.jpg"
                    class="login-img"
                    alt="ootp-beach-1"
                    border="0"
                  />
                </div>
              </div>
            </div>
          </div>
          <!-- end card-body -->
        </div>
        <!-- end card -->

        <p class="text-muted text-center mt-3 mb-0">
          Already have an account?
          <router-link to="/login" class="text-primary ml-1">Login</router-link>
        </p>

        <!-- end row -->
      </div>
      <!-- end col -->
    </div>
    <!-- Row -->
  </div>
</template>

<script>
export default {
  data() {
    return {
      name: "",
      email: "",
      contact: "",
      password: "",
    };
  },
  methods() {
    fetch("https://api-new-hotel.herokuapp.com/register", {
      method: "POST",
      body: JSON.stringify({
        name: this.name,
        email: this.email,
        contact: this.contact,
        password: this.password,
      }),
      headers: {
        "Content-type": "application/json; charset=UTF-8",
      },
    })
      .then((response) => response.json())
      .then((json) => {
        alert("User registered");
        localStorage.setItem("jwt", json.jwt);
        this.$router.push({ name: "Login" });
      })
      .catch((err) => {
        alert(err);
      });
  },
};
</script>

<style>
.account-block {
  padding: 0;
  background-image: url(https://bootdey.com/img/Content/bg1.jpg);
  background-repeat: no-repeat;
  background-size: cover;
  height: 480px;
  position: relative;
}

.pt-5 {
  height: 480px;
}

.login-img {
  height: 480px;
  width: 550px;
}

.account-block .overlay {
  -webkit-box-flex: 1;
  -ms-flex: 1;
  flex: 1;
  position: absolute;
  top: 0;
  bottom: 0;
  left: 0;
  right: 0;
  background-color: rgba(0, 0, 0, 0.4);
}
.account-block .account-testimonial {
  text-align: center;
  color: #fff;
  position: absolute;
  margin: 0 auto;
  padding: 0 1.75rem;
  bottom: 3rem;
  left: 0;
  right: 0;
}

.text-theme {
  color: #5369f8 !important;
}
.container {
  margin-top: 200px;
}
.btn-theme {
  background-color: #5369f8;
  border-color: #5369f8;
  color: #fff;
}
</style>
