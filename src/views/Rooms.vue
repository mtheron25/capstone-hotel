<template>
  <div class="rooms">
    <!--Room 1-->
    <div class="card mb-3" style="max-width: 1000px">
      <div class="row g-0">
        <div class="col-md-4">
          <img src="" class="img-fluid rounded-start" alt="..." />
        </div>
        <div class="col-md-2">
          <h6>Luxurious Double Bed</h6>
        </div>
        <div class="col-md-6">
          <div class="card-body">
            <h5 class="card-title">R955</h5>
            <p class="card-text">pp/pn</p>
            <!-- <router-link :to="{ name: 'RoomDetails' }"
              ><button type="button" class="btn">
                <span>See more</span>
              </button></router-link
            > -->
            <router-link
              v-for="room of rooms"
              :key="room.avail_id"
              :to="{ name: 'RoomDetails', params: { id: room.avail_id } }"
            ></router-link>
          </div>
        </div>
      </div>
    </div>
    <!--Room 2-->
    <div class="card mb-3" style="max-width: 1000px">
      <div class="row g-0">
        <div class="col-md-4">
          <img src="" class="img-fluid rounded-start" alt="..." />
        </div>
        <div class="col-md-2">
          <h6>Luxurious Double Bed</h6>
        </div>
        <div class="col-md-6">
          <div class="card-body">
            <h5 class="card-title">R955</h5>
            <p class="card-text">pp/pn</p>
            <router-link :to="{ name: 'RoomDetails' }"
              ><button type="button" class="btn">
                <span>See more</span>
              </button></router-link
            >
          </div>
        </div>
      </div>
    </div>
    <!--Room 3-->
    <div class="card mb-3" style="max-width: 1000px">
      <div class="row g-0">
        <div class="col-md-4">
          <img src="" class="img-fluid rounded-start" alt="..." />
        </div>
        <div class="col-md-2">
          <h6>Luxurious Double Bed</h6>
        </div>
        <div class="col-md-6">
          <div class="card-body">
            <h5 class="card-title">R955</h5>
            <p class="card-text">pp/pn</p>
            <router-link :to="{ name: 'RoomDetails' }"
              ><button type="button" class="btn">
                <span>See more</span>
              </button></router-link
            >
          </div>
        </div>
      </div>
    </div>
    <!--Room 4-->
    <div class="card mb-3" style="max-width: 1000px">
      <div class="row g-0">
        <div class="col-md-4">
          <img src="" class="img-fluid rounded-start" alt="..." />
        </div>
        <div class="col-md-2">
          <h6>Luxurious Double Bed</h6>
        </div>
        <div class="col-md-6">
          <div class="card-body">
            <h5 class="card-title">R955</h5>
            <p class="card-text">pp/pn</p>
            <router-link :to="{ name: 'RoomDetails' }"
              ><button type="button" class="btn">
                <span>See more</span>
              </button></router-link
            >
          </div>
        </div>
      </div>
    </div>
    <!--Room 5-->
    <div class="card mb-3" style="max-width: 1000px">
      <div class="row g-0">
        <div class="col-md-4">
          <img src="" class="img-fluid rounded-start" alt="..." />
        </div>
        <div class="col-md-2">
          <h6>Luxurious Double Bed</h6>
        </div>
        <div class="col-md-6">
          <div class="card-body">
            <h5 class="card-title">R955</h5>
            <p class="card-text">pp/pn</p>
            <router-link :to="{ name: 'RoomDetails' }"
              ><button type="button" class="btn">
                <span>See more</span>
              </button></router-link
            >
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style scoped>
.rooms {
  height: auto;
  background-color: #f2c078;
}
h5 {
  font-size: 20px;
  font-weight: bold;
}

h6 {
  padding-top: 100px;
}

.btn {
  text-decoration: none;
  background-color: #d99ac5;
  text-transform: uppercase;
  color: white;
  font-size: 20 px;
  padding: 12px 38px;
  border-radius: 5px;
  text-align: center;
  transition: all 0.5s;
  cursor: pointer;
}

.btn:hover {
  background-color: #32021f;
}
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
  background-color: #32021f;
}

.btn:hover span:after {
  opacity: 1;
  right: 0;
}

.card {
  margin-left: auto;
  margin-right: auto;
  /* padding-top: 50px; */
  background: white;
  border: 2px solid;
  box-shadow: 8px 8px 15px #e4e4e4, 8px 8px 15px #ffffff;
}
</style>
