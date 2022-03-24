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
        class="collapse justify-content-end navbar-collapse"
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
  font-weight: bold;
}

.nav-link:active {
  color: brown;
}

/* .navbar-toggler {
  align-items: flex-end;
} */
</style>
