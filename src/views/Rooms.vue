<template>
  <div class="container">
    <h1>Our Famous Suites</h1>
    <div class="WPd">
      <div class="WPk">
        <div class="WPm">
          <div class="WPf">Check-in/Check-out</div>
          <button class="WPo">
            Select Dates<svg
              class="WPq"
              viewBox="0 0 13 13"
              title=""
              role="img"
            >
              <use
                xlink:href="/img/sprite.svg#icon-small-calendar-3bf10"
              ></use></svg
            ><svg class="WPr" viewBox="0 0 320 512" title="" role="img">
              <use xlink:href="/img/sprite.svg#icon-angle-down-5dae7"></use>
            </svg>
          </button>
        </div>
      </div>
      <div class="WPk">
        <div class="WPn">
          <div class="WPf">Adults</div>
          <div class="AWd">
            <button type="button" class="AWf minus-icon"></button
            ><span tabindex="0" class="AWg">2</span
            ><button type="button" class="AWe plus-icon"></button>
          </div>
          <input type="hidden" name="room0adultCount" value="2" />
        </div>
      </div>
      <div class="WPk">
        <div class="WPn">
          <div class="WPf">Children</div>
          <div class="AWd">
            <button type="button" class="AWf minus-icon"></button
            ><span tabindex="0" class="AWg">0</span
            ><button type="button" class="AWe plus-icon"></button>
          </div>
          <input type="hidden" name="room0childCount" value="0" />
          <div class="WPv"></div>
        </div>
      </div>
      <div class="WPk">
        <input type="hidden" name="roomData" value="0" />
        <div class="WPg">
          <button class="CVd CVg" disabled="" type="submit">
            <span class="">Check Availability</span>
          </button>
        </div>
      </div>
    </div>
    <div class="row g-5">
      <!--Room 1-->

      <div class="col-md-4">
        <div class="content">
          <div class="content-overlay"></div>
          <img
            class="content-image"
            src="https://i.ibb.co/hXVcwDX/Deluxe-Suite-Gulf-Hotel-Bahrain-696x522.jpg"
          />
          <div class="content-details fadeIn-bottom">
            <h3 class="content-title">Deluxe Suite</h3>
            <button type="button" class="btn">
              <span>See more</span>
            </button>
          </div>
        </div>
      </div>

      <!--Room 2-->
      <div class="col-md-4">
        <div class="content">
          <div class="content-overlay"></div>
          <img
            class="content-image"
            src="https://i.ibb.co/0sBh2QY/Pool-Villa-Aleenta-Phuket-696x522.jpg"
          />
          <div class="content-details fadeIn-bottom">
            <h3 class="content-title">The Villa</h3>
            <button type="button" class="btn">
              <span>See more</span>
            </button>
          </div>
        </div>
      </div>
      <!--Room 3-->
      <div class="col-md-4">
        <div class="content">
          <div class="content-overlay"></div>
          <img
            class="content-image"
            src="https://i.ibb.co/6NNr1HB/Water-Bungalow-Sandals-South-Coast-Jamaica.jpg"
          />
          <div class="content-details fadeIn-bottom">
            <h3 class="content-title">Overwater Bungalow</h3>

            <button type="button" class="btn">
              <span>See more</span>
            </button>
          </div>
        </div>
      </div>
    </div>
    <br /><br />
    <div class="row g-5">
      <!--Room 4-->
      <div class="col-md-4">
        <div class="content">
          <div class="content-overlay"></div>
          <img
            class="content-image"
            src="https://i.ibb.co/BqpmJdz/spa-suite-image.jpg"
          />
          <div class="content-details fadeIn-bottom">
            <h3 class="content-title">The Spa Suite</h3>
            <button type="button" class="btn">
              <span>See more</span>
            </button>
          </div>
        </div>
      </div>
      <!--Room 5-->
      <div class="col-md-4">
        <div class="content">
          <div class="content-overlay"></div>
          <img
            class="content-image"
            src="https://i.ibb.co/HVsSbr8/st-regis.jpg"
          />
          <div class="content-details fadeIn-bottom">
            <h3 class="content-title">The Royal Suite</h3>
            <button type="button" class="btn">
              <span>See more</span>
            </button>
          </div>
        </div>
      </div>
      <!--Room 6-->
      <div class="col-md-4">
        <div class="content">
          <div class="content-overlay"></div>
          <img
            class="content-image"
            src="https://i.ibb.co/xHT5zbj/Grand-Velas.jpg"
          />
          <div class="content-details fadeIn-bottom">
            <h3 class="content-title">The Imperial Suite</h3>
            <button type="button" class="btn">
              <span>See more</span>
            </button>
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
.container {
  margin-top: 200px;
  z-index: 1;
}

.title {
  color: #1a1a1a;
  text-align: center;
  margin-bottom: 10px;
}

h1 {
  margin-top: 30px;
}

.content {
  position: relative;
  width: 90%;
  max-width: 400px;
  margin: auto;
  overflow: hidden;
}

.WPd {
  position: relative;
  z-index: 2;
  display: none;
  min-height: 7.5rem;
  flex-direction: row;
  justify-content: space-around;
  padding: 1.375rem 0 0.75rem;
  background-color: #fff;
  text-align: left;
}

.content .content-overlay {
  background: rgba(0, 0, 0, 0.7);
  position: absolute;
  height: 99%;
  width: 100%;
  left: 0;
  top: 0;
  bottom: 0;
  right: 0;
  opacity: 0;
  -webkit-transition: all 0.4s ease-in-out 0s;
  -moz-transition: all 0.4s ease-in-out 0s;
  transition: all 0.4s ease-in-out 0s;
}

.content:hover .content-overlay {
  opacity: 1;
}

.content-image {
  width: 100%;
  height: 300px;
}

img {
  box-shadow: 1px 1px 5px 1px rgba(0, 0, 0, 0.1);
  border-radius: 5px;
}

.content-details {
  position: absolute;
  text-align: center;
  padding-left: 1em;
  padding-right: 1em;
  width: 100%;
  top: 50%;
  left: 50%;
  opacity: 0;
  -webkit-transform: translate(-50%, -50%);
  -moz-transform: translate(-50%, -50%);
  transform: translate(-50%, -50%);
  -webkit-transition: all 0.3s ease-in-out 0s;
  -moz-transition: all 0.3s ease-in-out 0s;
  transition: all 0.3s ease-in-out 0s;
}

.content:hover .content-details {
  top: 50%;
  left: 50%;
  opacity: 1;
}

.content-details h3 {
  color: #fff;
  font-weight: 500;
  letter-spacing: 0.15em;
  margin-bottom: 0.5em;
  /* text-transform: uppercase; */
}

.content-details p {
  color: #fff;
  font-size: 0.8em;
}

.fadeIn-bottom {
  top: 80%;
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
</style>
