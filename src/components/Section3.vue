<template>
  <section class="section-3">
    <div class="section-title">
      <h3>
        TECHNOLOGY I USE
      </h3>
      <input
        placeholder="Search what I use"
        v-model="search"
        v-on:input="filterFunction"
      />
    </div>
    <section-3-list :skills="skills" ref="child_comp" />
  </section>
</template>

<script>
import { ref } from "vue";
import Section3List from "./Section3_List.vue";
import Image_Javascript from "../assets/images/javascript.png";
import Image_Typescript from "../assets/images/typescript.png";
import Image_NodeJs from "../assets/images/nodejs.png";
import Image_ExpressJs from "../assets/images/expressjs.png";
import Image_NestJs from "../assets/images/nestjs.png";
import Image_MongoDB from "../assets/images/mongodb.png";
import Image_MySQL from "../assets/images/mysql.png";
import Image_NuxtJs from "../assets/images/nuxtjs.png";
import Image_VueJs from "../assets/images/vuejs.png";
import Image_React from "../assets/images/react.svg";
import Image_WebSocket from "../assets/images/websocket.png";
export default {
  data() {
    return {
      search: "",
      skills: [],
      dataSkills: [
        {
          name: "Javascript",
          image: Image_Javascript
        },
        {
          name: "TypeScript",
          image: Image_Typescript
        },
        {
          name: "NodeJs",
          image: Image_NodeJs
        },
        {
          name: "ExpressJs",
          image: Image_ExpressJs
        },
        {
          name: "NestJs",
          image: Image_NestJs
        },
        {
          name: "MongoDB",
          image: Image_MongoDB
        },
        {
          name: "MySQL",
          image: Image_MySQL
        },
        {
          name: "NuxtJs",
          image: Image_NuxtJs
        },
        {
          name: "VueJs",
          image: Image_VueJs
        },
        {
          name: "ReactJs",
          image: Image_React
        },
        {
          name: "React Native",
          image: Image_React
        },
        {
          name: "WebSocket",
          image: Image_WebSocket
        }
      ]
    };
  },
  setup() {
    const child_comp = ref();

    const clearFunc = () => {
      child_comp.value?.clearCount();
    };

    return { child_comp, clearFunc };
  },
  components: {
    Section3List
  },
  methods: {
    filterFunction() {
      this.clearFunc();
      let a = this.dataSkills.filter(x =>
        x.name.toLowerCase().includes(this.search.toLowerCase())
      );
      a.length > 0 ? (this.skills = a) : (this.skills = this.dataSkills);
    }
  },
  created() {
    this.filterFunction();
  }
};
</script>

<style scoped>
.section-3 {
  /* margin-bottom: 300px; */
  height: 800px;
}
.section-title {
  text-align: center;
  /* margin-bottom: 50px; */
}
.section-title h3 {
  margin-bottom: 20px;
  font-family: Dyuthi, "sans-serif";
  font-size: 72px;
  color: #e6e6e6ff;
}
.section-title input {
  width: 40%;
  padding: 10px 20px 10px 20px;
  background: #654062ff;
  border: 0;
  caret-color: white;
  color: white;
  letter-spacing: 10px;
  word-spacing: 5px;
}
.section-title input::placeholder {
  color: #f4f4f4ff;
  font-family: sans-serif;
  letter-spacing: 10px;
  word-spacing: 5px;
}
.section-title input:focus {
  outline: none !important;
  box-shadow: 0 0 10px #654062ff;
}
</style>
