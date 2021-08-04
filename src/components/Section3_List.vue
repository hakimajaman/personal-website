<template>
  <div
    class="listing-container"
    :style="{ left: list_scroll }"
    @mouseover="mousehover = true"
    @mouseleave="mousehover = false"
  >
    <div class="listing-list" v-for="(skill, index) in skills" :key="index">
      <div class="image-container">
        <img :src="skill.image" :alt="skill.name" />
      </div>
      <h1>{{ skill.name }}</h1>
    </div>
  </div>
</template>

<script>
export default {
  props: ["skills"],
  data() {
    return {
      mousehover: false,
      mousemove: 0,
      runscroll: false,
      count_scroll: -150,
      list_scroll: "-150px"
    };
  },
  methods: {
    clearCount() {
      this.count_scroll = 0;
      this.list_scroll = "0px";
    },
    scrollRight() {
      if (this.count_scroll === 0) return;
      if (this.runscroll && this.mousehover) {
        this.count_scroll += 5;
        this.list_scroll = this.count_scroll + "px";
        setTimeout(this.scrollRight, 50);
      }
    },
    scrollLeft() {
      if (this.count_scroll === -5200 && this.skills.length >= 10) {
        return;
      } else if (
        this.count_scroll === -3660 &&
        this.skills.length < 10 &&
        this.skills.length > 6
      ) {
        return;
      } else if (
        this.count_scroll === -2170 &&
        this.skills.length < 7 &&
        this.skills.length > 3
      ) {
        return;
      } else if (
        this.count_scroll === -510 &&
        this.skills.length >= 1 &&
        this.skills.length < 3
      ) {
        return;
      } else {
        if (this.runscroll && this.mousehover) {
          this.count_scroll -= 5;
          this.list_scroll = this.count_scroll + "px";
        }
      }
      if (this.runscroll && this.mousehover) {
        setTimeout(this.scrollLeft, 50);
      }
    },
    getMousePosition(event) {
      this.mousemove = event.clientX;
      if (this.mousemove < 300) {
        this.runscroll = true;
        this.scrollRight();
      } else if (this.mousemove > 1000) {
        this.runscroll = true;
        this.scrollLeft();
      } else {
        this.runscroll = false;
      }
    }
  },
  created() {
    document.addEventListener("mousemove", this.getMousePosition);
  }
};
</script>

<style scoped>
.listing-container {
  display: flex;
  padding: 30px 40px 0px 40px;
  position: absolute;
}
.listing-list {
  border: 2px solid #654062ff;
  display: flex;
  flex-direction: column;
  align-items: center;
  text-align: center;
  width: 470px;
  height: 570px;
  padding: 8px 0px 10px 0px;
  color: #ecececff;
  margin-right: 50px;
  transition: all 0.5s;
}
.listing-list::after {
  content: "";
  border: 2px solid #643e6052;
  position: absolute;
  width: 470px;
  height: 590px;
  z-index: -2;
  margin-left: 30px;
  transition: all 0.5s;
}
.listing-list:hover {
  background-color: #654062ff;
}
.listing-list:hover::after {
  width: 470px;
  height: 570px;
  margin-left: 0;
}
.listing-list h1 {
  margin: 0;
  font-size: 50px;
  font-family: gubbi, sans-serif;
  font-weight: 300;
}
.listing-list img {
  width: 250px;
  margin-bottom: 60px;
  margin-top: 10px;
}
.image-container {
  height: 300px;
  display: inline-flex;
  align-items: center;
  justify-content: center;
}
</style>
