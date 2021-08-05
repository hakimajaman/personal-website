<template>
  <section class="section">
    <div class="text">
      <h1>Want to hire me?</h1>
    </div>
    <div class="button">
      <button>CLICK ME TO HIRE</button>
    </div>
  </section>
</template>

<style scoped>
.section {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  background: #f40968ff;
  height: 95vh;
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
