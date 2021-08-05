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
import Image_NuxtJs from "../assets/images/nuxtjs.png";
import Image_NodeJs from "../assets/images/nodejs.png";
import Image_PostgreSQL from "../assets/images/postgresql.png";
import Image_React from "../assets/images/react.svg";
import Image_NestJs from "../assets/images/nestjs.png";
import Image_MongoDB from "../assets/images/mongodb.png";
import Image_ExpressJs from "../assets/images/expressjs.png";
import Image_VueJs from "../assets/images/vuejs.png";
import Image_Flutter from "../assets/images/flutter.png";
import Image_HTML from "../assets/images/html5.png";
import Image_CSS from "../assets/images/css.png";
export default {
  components: {
    Section5List
  },
  data() {
    return {
      experiences: [
        {
          name: "No Travel No Life",
          position: "Front-End Developer",
          task: "Create client apps for travellers, it's like social media.",
          picture: null,
          alt: "NTNL",
          technology: [
            {
              name: "NuxtJs",
              picture: Image_NuxtJs
            },
            {
              name: "NodeJs",
              picture: Image_NodeJs
            },
            {
              name: "PostgreSQL",
              picture: Image_PostgreSQL
            }
          ]
        },
        {
          name: "Rumah Tahfidz Umar bin Khattab Batam",
          position: "Fullstack Developer",
          task:
            "Create backend, front-end, and the android apps for teacher attendance.",
          picture: Image_RTUBK,
          alt: "RTUBK",
          technology: [
            {
              name: "ReactJs",
              picture: Image_React
            },
            {
              name: "React Native",
              picture: Image_React
            },
            {
              name: "NestJs",
              picture: Image_NestJs
            },
            {
              name: "MongoDB",
              picture: Image_MongoDB
            }
          ]
        },
        {
          name: "Glints Academy x Binar",
          position: "Front-End Developer",
          task:
            "Learn about front-end developer with HTML, CSS, CSS Preprocessor, CSS Framework, ReactJs, Git, etc.",
          picture: Image_GlintsXBinar,
          alt: "GlitsXBinar",
          technology: [
            {
              name: "ReactJs",
              picture: Image_React
            }
          ]
        },
        {
          name: "Glints Academy x Binar",
          position: "Back-End Developer",
          task:
            "Learn about back-end developer with NodeJs, ExpressJs, MongoDB, etc. Create a REST APIs, etc.",
          picture: Image_GlintsXBinar,
          alt: "GlitsXBinar",
          technology: [
            {
              name: "ExpressJs",
              picture: Image_ExpressJs
            },
            {
              name: "NodeJs",
              picture: Image_NodeJs
            }
          ]
        },
        {
          name: "Politeknik Negeri Batam",
          position: "Diploma 3 - Technology Information",
          task:
            "Learn, Do and Get my diploma 3 by creating last apps with my team, the apps called re-visit.",
          picture: Image_Poltek,
          alt: "Polibatam",
          technology: [
            {
              name: "VueJs",
              picture: Image_VueJs
            },
            {
              name: "NodeJs",
              picture: Image_NodeJs
            },
            {
              name: "MongoDB",
              picture: Image_MongoDB
            },
            {
              name: "Flutter",
              picture: Image_Flutter
            }
          ]
        },
        {
          name: "PT. Schneider Electric Manufacturing Batam",
          position: "Helpdesk IT Support",
          task:
            "Help the IT Support to fix computer, and update software, etc.",
          picture: Image_Schneider,
          alt: "Schneider-Electric",
          technology: []
        },
        {
          name: "Batam Linux User Group",
          position: "Member Education",
          task: "Teach and learn about linux, open source software, etc.",
          picture: Image_BLUG,
          alt: "BLUG",
          technology: []
        },
        {
          name: "Vocational High School 5 Batam",
          position: "Student - Computer Engineering",
          task: "Learn about Networking, Linux and HTML & CSS.",
          picture: Image_SMK,
          alt: "SMKN5Batam",
          technology: [
            {
              name: "HTML",
              picture: Image_HTML
            },
            {
              name: "CSS",
              picture: Image_CSS
            }
          ]
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
  height: 850px;
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
