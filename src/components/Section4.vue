<template>
  <section class="section">
    <div class="section-text">
      <h1>Connect</h1>
      <h1>with</h1>
      <h1>me</h1>
    </div>
    <div class="section-image">
      <div class="image-link">
        <div>
          <a href="google.com">
            <img :src="gitlab" alt="gitlab.com/hakimajaman" />
            <span>Gitlab</span>
          </a>
        </div>
        <div>
          <a href="google.com">
            <img :src="github" alt="github.com/hakimajaman" />
            <span>Github</span>
          </a>
        </div>
        <div>
          <a href="google.com">
            <img
              :src="linkedin"
              alt="linkedin.com/in/rifqi-taufiqul-hakim-6806bb194"
            />
            <span>LinkedIn</span>
          </a>
        </div>
      </div>
      <div class="image-gmail">
        <img :src="gmail" alt="rifqitaufiqulhakim199922@gmail.com" />
        <span>rifqitaufiqulhakim199922@gmail.com</span>
      </div>
    </div>
  </section>
</template>

<script>
import Image_Gitlab from "../assets/images/gitlab.png";
import Image_Github from "../assets/images/github.png";
import Image_Linkedin from "../assets/images/linkedin.png";
import Image_Gmail from "../assets/images/gmail.png";
export default {
  data() {
    return {
      gitlab: Image_Gitlab,
      github: Image_Github,
      linkedin: Image_Linkedin,
      gmail: Image_Gmail
    };
  }
};
</script>

<style scoped>
.section {
  height: 500px;
  display: flex;
  align-items: center;
  justify-content: center;
}
.section h1 {
  color: #e6e6e6ff;
  margin: 0;
  font-size: 50px;
  font-family: dyuthi, sans-serif;
  font-weight: 300;
}
.section img {
  width: 50px;
  height: 50px;
}
.section-text {
  width: 350px;
}
.section-image {
  width: 300px;
}
.image-link {
  display: flex;
  margin-bottom: 30px;
}
.image-link div {
  padding-right: 20px;
}
.image-link div a {
  display: inline-flex;
  align-items: center;
  color: #20194aff;
  text-decoration: none;
  font-family: sans-serif;
}
.image-link div a span {
  display: none;
}
.image-link div:hover {
  background: #fb9dc3ff;
  border-radius: 50px;
  margin-right: 50px;
}
.image-link div:last-child:hover {
  margin-right: 0px;
}
.image-link div:hover a span {
  display: block;
}
.image-gmail {
  display: inline-flex;
  align-items: center;
  color: #ecececff;
}
.image-gmail img {
  height: 30px;
  width: 30px;
  margin-right: 15px;
}
</style>
