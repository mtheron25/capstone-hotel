<template>
  <div class="container">
    <div class="col-md-4">
      <div class="content">
        <div class="content-overlay"></div>
        <img
          class="content-image"
          src="https://i.ibb.co/hXVcwDX/Deluxe-Suite-Gulf-Hotel-Bahrain-696x522.jpg"
        />
        <div class="content-details fadeIn-bottom">
          <h3 class="content-title">Deluxe Suite</h3>
          <router-link :to="{ name: 'RoomDetails' }"
            ><button type="button" class="btn">
              <span>See more</span>
            </button></router-link
          >
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style scoped></style>
