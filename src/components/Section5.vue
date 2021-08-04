<template>
  <section class="section">
    <div class="shadow"></div>
    <div class="section-title">
      <h3>
        EXPERIENCES
      </h3>
    </div>
    <section-5-list :experiences="experiences" />
  </section>
</template>

<script>
import Section5List from "./Section5_List.vue";
import Image_RTUBK from "../assets/images/rtubk.png";
import Image_GlintsXBinar from "../assets/images/glintsXbinar.png";
import Image_Schneider from "../assets/images/schneider.png";
import Image_BLUG from "../assets/images/blug.jpeg";
import Image_Poltek from "../assets/images/poltek.png";
import Image_SMK from "../assets/images/smkn5batam.jpg";
export default {
  components: {
    Section5List
  },
  data() {
    return {
      experiences: [
        {
          name: "Rumah Tahfidz Umar bin Khattab Batam",
          position: "Fullstack Developer",
          task:
            "Create backend, front-end, and the android apps for teacher attendance.",
          picture: Image_RTUBK,
          technology: "reactjs, react native, nestjs, mongodb"
        },
        {
          name: "No Travel No Life",
          position: "Front-End Developer",
          task: "Create client apps for travellers, it's like social media.",
          picture: null,
          technology: "nuxtjs, nodejs, postgresql"
        },
        {
          name: "Glints Academy x Binar",
          position: "Front-End Developer",
          task: "Learn about front-end developer.",
          picture: Image_GlintsXBinar,
          technology: "reactjs"
        },
        {
          name: "Glints Academy x Binar",
          position: "Back-End Developer",
          task: "Learn about back-end developer",
          picture: Image_GlintsXBinar,
          technology: "nodejs, expressjs"
        },
        {
          name: "Politeknik Negeri Batam",
          position: "Diploma 3 - Technology Information",
          task:
            "Learn, Do and Get my diploma 3 by creating last apps with my team, the apps called re-visit.",
          picture: Image_Poltek,
          technology: "vuejs, nodejs, mongodb, flutter"
        },
        {
          name: "PT. Schneider Electric Manufacturing Batam",
          position: "Helpdesk IT Support",
          task:
            "Help the IT Support to fix computer, and update software, etc.",
          picture: Image_Schneider,
          technology: null
        },
        {
          name: "Batam Linux User Group",
          position: "Member Education",
          task: "Teach and learn about linux, open source software, etc.",
          picture: Image_BLUG,
          technology: null
        },
        {
          name: "Vocational High School 5 Batam",
          position: "Student - Computer Engineering",
          task: "Learn about Networking, Linux and HTML & CSS.",
          picture: Image_SMK,
          technology: "html, css"
        }
      ]
    };
  }
};
</script>

<style scoped>
.shadow {
  background-image: linear-gradient(
    transparent,
    #2a205700,
    rgba(0, 0, 0, 0.3),
    rgba(0, 0, 0, 0.3),
    #2a205700
  );
  position: absolute;
  width: 100%;
  height: 100%;
  z-index: 1;
}
.section {
  margin-bottom: 500px;
}
.section-title {
  text-align: center;
}
.section-title h3 {
  margin-top: 20px;
  margin-bottom: 20px;
  font-family: Dyuthi, "sans-serif";
  font-size: 72px;
  color: #e6e6e6ff;
}
</style>
