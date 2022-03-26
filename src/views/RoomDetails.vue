<template>
  <div v-if="room">
    <div class="room">
      <img class="content-image" :src="room.room_img" :alt="room.room_name" />
      <div class="blog-details">
        <h2>{{ room.room_name }}</h2>
        <h4>{{ room.room_price }}</h4>
        <p>{{ room.room_desc }}</p>
      </div>
    </div>
  </div>
  <div v-else>Loading the rooms...</div>
</template>

<script>
export default {};
</script>

<style></style>
