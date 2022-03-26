<template>
  <div class="container-fluid">
    <nav class="navbar navbar-expand-lg navbar-light">
      <button
        class="navbar-toggler"
        type="button"
        data-bs-toggle="collapse"
        data-bs-target="#navbarNavAltMarkup"
        aria-controls="navbarNavAltMarkup"
        aria-expanded="false"
        aria-label="Toggle navigation"
      >
        <span class="navbar-toggler-icon"></span>
      </button>
      <div
        class="collapse justify-content-start navbar-collapse"
        id="navbarNavAltMarkup"
      >
        <div class="navbar-nav">
          <li class="nav-item">
            <router-link class="nav-link" aria-current="page" to="/"
              >Home</router-link
            >
          </li>
          <li class="nav-item">
            <router-link class="nav-link" aria-current="page" to="/about"
              >About</router-link
            >
          </li>
          <li class="nav-item">
            <router-link class="nav-link" aria-current="page" to="/contact"
              >Contact</router-link
            >
          </li>
        </div>
      </div>
      <div class="dropdown">
        <button
          class="btn btn-secondary rounded-circle dropdown-toggle"
          type="button"
          id="dropdownMenuButton1"
          data-bs-toggle="dropdown"
          aria-expanded="false"
        >
          <i class="fa fa-user" aria-hidden="true"></i>
        </button>
        <ul class="dropdown-menu" aria-labelledby="dropdownMenuButton1">
          <li>
            <router-link class="dropdown-item" to="/login">Login</router-link>
          </li>
          <li><hr class="dropdown-divider" /></li>
          <li>
            <router-link class="dropdown-item" to="/register"
              >Sign Up</router-link
            >
          </li>
        </ul>
      </div>
    </nav>
  </div>
</template>

<script>
export default {};
</script>

<style scoped>
.container-fluid {
  width: 100%;
  top: 0;
  position: fixed;
  background-color: #f2c078;
  /* background-color: transparent !important; */
  border-color: #e7e7e7;
  padding: 2px;
}

.collapse {
  padding-right: 50px;
}

.nav-link {
  font-size: 25px;
  color: white;
  /* font-weight: bold; */
}

.nav-link:active {
  color: brown;
}

.dropdown-menu {
  width: 5px;
  left: -200%;
}

/* .navbar-toggler {
  align-items: flex-end;
} */
</style>
