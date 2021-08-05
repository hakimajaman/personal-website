<template>
  <footer class="footer">
    <div>
      <h1>RIFQI TAUFIQUL HAKIM © 2021</h1>
    </div>
    <div>
      <div>
        <img :src="images[0]" alt="rifqitaufiqulhakim199922@gmail.com" />
        <h2>rifqitaufiqulhakim199922@gmail.com</h2>
      </div>
    </div>
  </footer>
</template>

<script>
import Image_Gmail from "../assets/images/gmail.png";
export default {
  data() {
    return {
      images: [Image_Gmail]
    };
  }
};
</script>

<style scoped>
.footer {
  background-color: #b9064eff;
  padding: 20px 100px 10px 100px;
  display: flex;
  align-items: center;
}
.footer h1 {
  margin: 0;
  color: #f4f4f4;
  font-size: 20px;
  font-family: gubbi, sans-serif;
  font-weight: 300;
  letter-spacing: 5px;
  word-spacing: 1.25px;
}
.footer h2 {
  margin: 0;
  color: #f4f4f4;
  font-size: 15px;
  font-family: gubbi, sans-serif;
  font-weight: 300;
  letter-spacing: 5px;
  word-spacing: 1.25px;
}
.footer div:last-child {
  margin-left: auto;
}
.footer div:last-child div {
  display: inline-flex;
  align-items: center;
}
.footer div img {
  width: 20px;
  margin-right: 20px;
  margin-bottom: 5px;
}
</style>
