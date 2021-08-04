<template>
  <section class="section">
    <div
      class="type-writing"
      :class="{ 'typing-1': typing[0], 'typing-2': typing[1] }"
    >
      <h1>{{ letter[0] }}</h1>
      <div>
        <span
          ><h3>{{ letter[1] }}</h3></span
        >
        <span style="color: #f40968ff"
          ><h3>{{ letter[2] }}</h3></span
        >
        <span style="color: #f7e018ff"
          ><h3>{{ letter[3] }}</h3></span
        >
        <span
          ><h3>{{ letter[4] }}</h3></span
        >
      </div>
    </div>
  </section>
</template>

<script>
export default {
  data() {
    return {
      text: [
        "HELLO, MY NAME IS HAKIM",
        "I am",
        "Fullstack",
        "Javascript",
        "Developer."
      ],
      count: 0,
      index: 0,
      letter: ["", "", "", "", ""],
      remove: false,
      typing: [true, false],
      fullClearing: true
    };
  },
  methods: {
    runClearingFull() {
      if (this.index < 0) {
        this.index = 0;
        setTimeout(this.runScripting, 1000);
      } else if (this.letter[this.index].length === 0) {
        this.index--;
        if (this.index === 0) {
          this.typing[1] = false;
          this.typing[0] = true;
        }
        setTimeout(this.runClearingFull, 50);
      } else {
        this.letter[this.index] = this.letter[this.index].substring(
          0,
          this.letter[this.index].length - 1
        );
        setTimeout(this.runClearingFull, 50);
      }
    },
    runClearingHalf() {
      if (this.letter[0].length === 19) {
        this.count = this.letter[0].length;
        setTimeout(this.runScripting, 700);
      } else if (this.letter[this.index].length === 0) {
        this.index--;
        if (this.index === 0) {
          this.typing[1] = false;
          this.typing[0] = true;
          this.count = this.letter[this.index].length - 1;
        }
        setTimeout(this.runClearingHalf, 50);
      } else {
        this.letter[this.index] = this.letter[this.index].substring(
          0,
          this.letter[this.index].length - 1
        );
        setTimeout(this.runClearingHalf, 50);
      }
    },
    runScripting() {
      if (this.text[this.index]) {
        if (this.count === this.text[this.index].length) {
          this.typing[this.index] = false;
          this.index++;
          if (this.index === this.text.length) {
            this.count = 0;
            this.index--;
            this.remove = false;
            this.fullClearing = !this.fullClearing;
            this.fullClearing
              ? setTimeout(this.runClearingFull, 3000)
              : setTimeout(this.runClearingHalf, 3000);
          } else {
            this.typing[1] = true;
            this.count = 0;
            setTimeout(this.runScripting, 80);
          }
        } else {
          let char = this.text[this.index][this.count];
          if (this.index === 0 && this.count === 12 && !this.remove) {
            char = "N";
          }
          if (this.index === 0 && this.count === 14 && !this.remove) {
            setTimeout(() => {
              this.letter[0] = this.letter[0].substring(
                0,
                this.letter[0].length - 1
              );
              this.count = this.count - 2;
              setTimeout(() => {
                this.letter[0] = this.letter[0].substring(
                  0,
                  this.letter[0].length - 1
                );
                this.remove = true;
                setTimeout(this.runScripting, 550);
              }, 200);
            }, 1000);
          } else {
            this.letter[this.index] += char;
            this.count++;
            setTimeout(this.runScripting, 80);
          }
        }
      }
    }
  },
  created() {
    this.runScripting();
  }
};
</script>

<style scoped>
.section {
  color: white;
  height: 900px;
  justify-content: center;
  align-items: center;
  display: flex;
}

.section h1 {
  margin: 0;
  font-size: 100px;
  letter-spacing: 1px;
  color: #fff;
  font-family: suruma, sans-serif;
}

.section h3 {
  margin: 0;
  font-size: 64px;
  font-family: gubbi, sans-serif;
  font-weight: 300;
}

.type-writing {
  text-align: center;
  height: 100px;
}

.type-writing span {
  display: inline-block;
  margin-right: 20px;
}

.type-writing h1::after {
  content: "";
  position: absolute;
  border-right: 2px solid gold;
  height: 80px !important;
  animation: blink 1s infinite ease;
  display: none;
}

.typing-1 h1::after {
  display: inline;
}

.type-writing div::after {
  content: "";
  position: absolute;
  border-right: 2px solid gold;
  margin-left: -20px;
  height: 80px !important;
  animation: blink 2s infinite ease;
  display: none;
}

.typing-2 div::after {
  display: inline;
}

@keyframes blink {
  0% {
    opacity: 0;
  }
  100% {
    opacity: 100;
  }
}
</style>
