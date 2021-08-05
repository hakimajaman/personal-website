<template>
  <div class="container" :style="{ left: list_scroll }">
    <div
      class="box"
      :class="{
        'primary-box': index + 1 === select,
        'prev-box': select > index + 1,
        'next-box': select < index + 1
      }"
      v-for="(data, index) in experiences"
      :key="index"
    >
      <div class="image-container">
        <div class="logo">
          <img :src="data.picture" :alt="data.alt" v-if="data.picture" />
          <h1 v-if="!data.picture" class="alt-text">{{ data.alt }}</h1>
        </div>
        <div class="technology-container">
          <div
            class="technology-column"
            v-for="(img, idx) in data.technology"
            :key="idx"
          >
            <div>
              <img :src="img.picture" :alt="img.name" />
            </div>
            <span>{{ img.name }}</span>
          </div>
        </div>
      </div>
      <div>
        <h1>{{ data.position }}</h1>
        <h1>{{ data.task }}</h1>
      </div>
    </div>
  </div>
  <div class="button-container">
    <div
      class="button button-left"
      @click="slide_left"
      :style="{ display: select === 1 ? 'none' : 'block' }"
    >
      <h2>‹</h2>
    </div>
    <div
      class="button button-right"
      @click="slide_right"
      :style="{ display: select === experiences.length ? 'none' : 'block' }"
    >
      <h2>›</h2>
    </div>
  </div>
</template>

<script>
export default {
  props: ["experiences"],
  data() {
    return {
      datas: [1, 2, 3, 4, 5],
      select: 2,
      count_scroll: -45,
      list_scroll: "-45%" /* tambah 70 untuk kelanjutan dari 50 */
    };
  },
  methods: {
    slide_right() {
      if (this.select === this.experiences.length) {
        return;
      }
      this.count_scroll = this.count_scroll - 70;
      this.list_scroll = this.count_scroll + "%";
      this.select += 1;
    },
    slide_left() {
      if (this.select === 1) {
        return;
      }
      this.count_scroll = this.count_scroll + 70;
      this.list_scroll = this.count_scroll + "%";
      this.select -= 1;
    }
  }
};
</script>

<style scoped>
.button-container {
  z-index: 3;
  position: absolute;
  width: 100%;
  display: inline-flex;
  padding-top: 150px;
}
.button-container h2 {
  font-size: 50px;
  border: 2px solid #503b93;
  border-radius: 100%;
  height: 75px;
  width: 80px;
  padding-top: 5px;
  transition: all 0.2s;
  user-select: none;
}
.button {
  position: absolute;
  text-align: center;
}
.button h2:hover {
  background: #7b65c1;
  cursor: pointer;
  color: #ecececff;
}
.button-left {
  left: 100px;
}
.button-right {
  right: 100px;
}
.container {
  display: inline-flex;
  justify-content: center;
  height: 50em;
  position: absolute;
  transition: all 0.5s ease;
}
.box {
  width: 60em;
  height: 70%;
  margin-right: 200px;
  transition: all 0.5s ease;
  border-radius: 5px;
  display: flex;
}
.box div {
  text-align: left;
}
.box div h1:first-child {
  margin-top: 60px;
}
.box div h1 {
  margin: 0;
  margin-bottom: 20px;
  font-size: 50px;
  font-family: dyuthi, sans-serif;
  font-weight: 300;
}
.image-container {
  display: flex;
  flex-direction: column;
  width: 40%;
}
.logo {
  margin-right: 80px;
}
.logo img {
  width: 200px;
  margin-left: 80px;
  margin-top: 50px;
}
.primary-box {
  background-image: linear-gradient(
    to bottom right,
    rgba(81, 46, 94, 0.1),
    #2b214b
  );
  z-index: 2;
  box-shadow: 5px 10px rgba(22, 17, 51, 0.5);
}
.primary-box div h1 {
  color: white;
}
.primary-box div h1:first-child {
  color: #f40968ff;
}
.prev-box {
  margin-top: 130px;
  background-image: linear-gradient(
    to left bottom,
    rgba(81, 46, 94, 0.1),
    #2b2155,
    rgba(0, 0, 0, 0.5)
  );
}
.next-box {
  margin-top: 130px;
  background-image: linear-gradient(
    to left bottom,
    rgba(81, 46, 94, 0.1),
    #2b2155,
    rgba(0, 0, 0, 0.5)
  );
}
.prev-box img {
  filter: grayscale(100%);
}
.prev-box div h1 {
  color: transparent;
}
.next-box img {
  filter: grayscale(100%);
}
.next-box div h1 {
  color: transparent;
}
.technology-container {
  display: flex;
  align-items: center;
  flex-wrap: wrap;
  margin-top: auto;
  margin-bottom: 30px;
  margin-left: 50px;
}
.technology-column {
  margin-right: 40px;
  margin-bottom: 40px;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  color: #ecececff;
}
.technology-column div {
  height: 35px;
}
.technology-column div:last-child {
  margin-right: 0px;
}
.technology-column div img {
  width: 30px;
  filter: grayscale(100%);
}
</style>
