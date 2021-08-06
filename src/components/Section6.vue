<template>
  <section class="section">
    <!-- <div
      class="first-layer-container"
      :class="{ 'hide-first-layer': click_now }"
    >
      <div class="first-layer-row">
        <div class="text">
          <h1>Want to hire me?</h1>
        </div>
        <div class="button">
          <button @click="click_method">CLICK ME TO HIRE</button>
        </div>
      </div>
    </div> -->
    <div class="second-layer-container">
      <div class="second-layer-row">
        <div class="text-second">
          <h1>Dear Recruiter:</h1>
          <p>
            Lorem ipsum dolor sit amet consectetur adipisicing elit. Deleniti
            modi sit nihil ut enim! Error eius, quo doloribus vel fugiat
            corporis quas in consequatur, iusto dolor porro expedita, similique
            commodi?
          </p>
        </div>
        <form class="form-second">
          <div class="lock-form"></div>
          <h5>I Will Email You!</h5>
          <div>
            <span>Full Name</span>
            <input placeholder="Full Name" />
          </div>
          <div>
            <span>Email</span>
            <input placeholder="Email" />
          </div>
          <div>
            <span>Company</span>
            <input placeholder="Company" />
          </div>
          <div>
            <span>Message</span>
            <textarea placeholder="Message" />
          </div>
          <div class="form-button">
            <button>SUBMIT</button>
          </div>
        </form>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  data() {
    return {
      click_now: false
    };
  },
  methods: {
    click_method() {
      this.click_now = !this.click_now;
    }
  }
};
</script>

<style scoped>
.section {
  min-height: 120vh;
  background: #f40968ff;
}
.first-layer-container {
  position: absolute;
  left: 50%;
  width: 100%;
  margin-top: 10%;
  transition: all 0.7s ease;
}
.first-layer-row {
  display: flex;
  flex-direction: column;
  align-items: center;
  position: relative;
  left: -50%;
}
.hide-first-layer {
  left: 150%;
}
.lock-form {
  height: 100%;
  background: rgba(0, 0, 0, 0.5);
  position: absolute;
  padding: 20px;
}
.second-layer-container {
  position: absolute;
  width: 100%;
  margin-top: 50px;
  transition: all 0.7s ease;
}
.second-layer-row {
  display: flex;
  align-items: center;
  position: relative;
  padding-left: 5%;
  padding-right: 5%;
}
.text-second {
  width: 40%;
}
.text-second h1 {
  margin: 0;
  color: #1f2126;
  font-size: 40px;
  font-family: gubbi, sans-serif;
  font-style: italic;
}
.text-second p {
  color: #1f2126;
  font-size: 30px;
  font-family: sans-serif;
  word-spacing: 10px;
  word-break: inherit;
  text-align: justify;
  text-indent: 30px;
}
.form-second {
  margin-left: auto;
  width: 50%;
}
.form-second h5 {
  text-align: center;
  font-size: 30px;
  color: rgb(240, 203, 203);
  letter-spacing: 7px;
  font-family: "Courier New", Courier, monospace;
}
.form-button button {
  position: relative;
  left: 25%;
  transition: all 0.2s ease-in;
}
.form-button button {
  width: 50%;
  height: 40px;
  background-color: #b9064eff;
  border: 0;
  color: white;
  letter-spacing: 10px;
  box-shadow: 3px 5px rgba(185, 6, 78, 0.4);
}
.form-button button:hover {
  background-color: rgb(213, 36, 107);
}
.form-second div {
  margin-bottom: 50px;
  display: flex;
  flex-direction: column;
}
.form-second div:last-child {
  margin-bottom: 0;
}
.form-second span {
  color: #f7f1f1;
  font-size: 18px;
  letter-spacing: 5px;
  font-weight: bold;
  transition: all 0.5s ease-in;
}
.form-second input {
  border: 2px solid #7c164eff;
  width: 100%;
  height: 60px;
  padding: 0px 10px 5px 10px;
  margin-right: 30px;
  background: transparent;
  font-size: 30px;
  outline: none;
  color: white;
  margin-top: 10px;
}
.form-second input::placeholder {
  color: #d6cccc;
  font-size: 20px;
  vertical-align: middle;
}
.form-second textarea {
  border: 2px solid #7c164eff;
  width: 100%;
  min-height: 80px;
  padding: 5px 10px 5px 10px;
  margin-right: 30px;
  background: transparent;
  font-size: 20px;
  outline: none;
  color: white;
  margin-top: 10px;
}
.form-second textarea::placeholder {
  color: #d6cccc;
  font-size: 20px;
  vertical-align: middle;
}
.text h1 {
  margin: 0;
  color: #f4f4f4;
  font-size: 104px;
  font-family: gubbi, sans-serif;
  font-weight: 300;
}
.button button {
  border-radius: 50px;
  font-size: 40px;
  font-family: sans-serif;
  letter-spacing: 10px;
  word-spacing: 1.25px;
  padding: 10px 50px 10px 50px;
  background: transparent;
  border: 5px solid #7c164eff;
  color: #f4f4f4;
  transition: all 0.2s ease-in;
  cursor: pointer;
}
.button button:hover {
  background: #7c164eff;
  color: #f40968ff;
  border-color: #f40968ff;
}
</style>
