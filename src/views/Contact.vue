<template>
  <div class="contact">
    <div class="contact-form">
      <h7>Let's get in touch</h7>
      <form @submit.prevent="handleSubmit">
        <label>Name:</label>
        <input type="name" v-model="name" />
        <label>Email</label>
        <input type="email" v-model="email" />
        <label>Mobile</label>
        <input type="contact" v-model="contact" />
        <label>Message:</label><br />
        <textarea name="message" v-model="message"></textarea>
        <div class="button">
          <button type="submit">Submit Message</button>
          <button type="reset">Reset</button>
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
      email: "",
      message: "",
    };
  },
  methods: {
    handleSubmit() {
      console.log(
        this.name,
        this.surname,
        this.email,
        this.contact,
        this.messsage
      );
      fetch("https://jsonplaceholder.typicode.com/posts", {
        method: "POST",
        body: JSON.stringify({
          title: "foo",
          body: "bar",
          userId: 1,
        }),
        headers: {
          "Content-type": "application/json; charset=UTF-8",
        },
      })
        .then((response) => response.json())
        .then((json) => console.log(json));
    },
  },
};
</script>

<style scoped>
.contact {
  height: 100vh;
  width: 100%;
  background: linear-gradient(0deg, rgba(0, 0, 0, 0.7), rgba(0, 0, 0, 0.7)),
    url(https://images.mrandmrssmith.com/images/1482x988/3634023-one-and-only-the-palm-hotel-dubai-united-arab-emirates.jpg);
  background-size: cover;
  background-attachment: fixed;
}
.contact-form {
  padding-top: 150px;
}
form {
  max-width: 450px;
  margin: 30px auto;
  text-align: left;
  padding: 40px;
  /* From https://css.glass */
  background: rgba(86, 77, 128, 0.19);
  border-radius: 16px;
  box-shadow: 0 4px 30px rgba(0, 0, 0, 0.1);
  backdrop-filter: blur(7.9px);
  -webkit-backdrop-filter: blur(7.9px);
  border: 1px solid rgba(86, 77, 128, 0.22);
}
h7 {
  font-size: 80px;

  color: white;
  font-weight: bolder;
  font-family: cursive;
}
textarea {
  width: 100%;
  height: 100px;
  background: #98A6D4;
}
label {
  color: white;
  display: inline-block;
  margin: 25px 0 15px;
  font-size: 10px;
  text-transform: uppercase;
  letter-spacing: 1px;
  font-weight: bold;
}
input {
  display: block;
  padding: 10px 6px;
  width: 100%;
  box-sizing: border-box;
  border: none;
  border-bottom: 1px solid #98A6D4;
  color: black;
  background: #98A6D4;
}

button {
  background: #44344F;
  border: 0;
  padding: 10px 20px;
  margin-top: 20px;
  color: white;
  border-radius: 20px;
  cursor: pointer;
  margin: 5px;
}
button:hover {
  opacity: 0.8;
}
.submit {
  text-align: center;
}
</style>
