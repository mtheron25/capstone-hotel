<template>
  <div class="home">
    <div class="heading">
      <h1>Hotel deLux</h1>
      <br />
      <h2>Not just nearly Luxury, but really Luxury</h2>
      <br /><br />

      <router-link :to="{ name: 'Rooms' }"
        ><button type="button" class="btn">
          <span>Explore</span>
        </button></router-link
      >
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style scoped>
.home {
  min-height: 100vh;
  background-color: #232323;
  background: linear-gradient(0deg, rgba(0, 0, 0, 0.7), rgba(0, 0, 0, 0.7)),
    url(https://images.mrandmrssmith.com/images/1482x988/3634023-one-and-only-the-palm-hotel-dubai-united-arab-emirates.jpg);
  background-size: cover;
}

.heading {
  width: 100%;
}

.btn {
  text-decoration: none;
  background-color: #bd9d6b;
  text-transform: uppercase;
  color: black;
  font-size: 20 px;
  padding: 12px 38px;
  border-radius: 5px;
  text-align: center;
  transition: all 0.5s;
  cursor: pointer;
  z-index: -1;
  font-weight: bold;
}

/* .btn:hover {
  background-color: #705d56;
} */
.btn span {
  cursor: pointer;
  display: inline-block;
  position: relative;
  transition: 0.5s;
}

.btn span:after {
  content: "\00bb";
  position: absolute;
  opacity: 0;
  top: 0;
  right: -20px;
  transition: 0.5s;
}

.btn:hover span {
  padding-right: 25px;
  /* background-color: #705d56; */
}

.btn:hover span:after {
  opacity: 1;
  right: 0;
}

h1 {
  font-weight: bolder;
  font-family: cursive;
  /* font-style: italic; */
  color: white;
  font-size: 150px;
  text-align: center;
  padding-top: 270px;
}

h2 {
  font-style: italic;
  font-family: cursive;
  color: white;
  font-size: 30px;
}
</style>
