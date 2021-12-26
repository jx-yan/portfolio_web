<template>
  <div class="row p-0 m-0 justify-content-center">
    <div
      class="message col-10 text-center animate__animated animate__backInLeft"
    >
      <h1 class="typed-text">
        {{ typeValue }}
        <div class="cursor" :class="{ typing: typeStatus }"></div>
      </h1>
      <br />

      <h2>This is <img class="logo-navbar" /></h2>
      <br />

      <h5>
        Information Systems
        <span class="year" v-html="year[2]"></span>
        in &nbsp;&nbsp;<img
          class="school-logo"
          src="../../assets/school_logo.png"
          alt="school-logo"
        />
      </h5>
    </div>
  </div>
</template>

<script>
export default {
  name: "Message",
  data() {
    return {
      name: "Jiaxing",
      year: {
        2: "Sophomore",
        3: "Penultimate",
        4: "Final",
      },
      typeValue: "",
      typeStatus: false,
      typeArray: [
        "Hello!",
        "你好!",
        "Bonjour!",
        "Hola!",
        "Ciao!",
        "こんにちは!",
        "안녕하세요!",
      ],
      typingSpeed: 150,
      erasingSpeed: 100,
      newTextDelay: 1000,
      typeArrayIndex: 0,
      charIndex: 0,
    };
  },
  methods: {
    typeText() {
      if (this.charIndex < this.typeArray[this.typeArrayIndex].length) {
        if (!this.typeStatus) {
          this.typeStatus = true;
        }
        this.typeValue += this.typeArray[this.typeArrayIndex].charAt(
          this.charIndex
        );
        this.charIndex += 1;
        setTimeout(this.typeText, this.typingSpeed);
      } else {
        this.typeStatus = false;
        setTimeout(this.eraseText, this.newTextDelay);
      }
    },
    eraseText() {
      if (this.charIndex > 0) {
        if (!this.typeStatus) {
          this.typeStatus = true;
        }
        this.typeValue = this.typeArray[this.typeArrayIndex].substring(
          0,
          this.charIndex - 1
        );
        this.charIndex -= 1;
        setTimeout(this.eraseText, this.erasingSpeed);
      } else {
        this.typeStatus = false;
        this.typeArrayIndex += 1;
        if (this.typeArrayIndex >= this.typeArray.length) {
          this.typeArrayIndex = 0;
        }
        setTimeout(this.typeText, this.typingSpeed + 1000);
      }
    },
  },
  created() {
    setTimeout(this.typeText, this.newTextDelay + 200);
  },
};
</script>

<style scoped>
@import url("https://fonts.googleapis.com/css2?family=Bakbak+One&display=swap");

.row {
  display: flex;
  align-items: center;
  justify-content: center;
  height: 100%;
}

.message {
  font-family: "Bakbak One", cursive;
  background: #fff;
  padding: 2rem;
  border-radius: 10px;
  box-shadow: 1px 3px 5px rgba(0, 0, 0, 0.1);
}

h1.typed-text {
  color: #6495ed;
}

div.cursor {
  display: inline-block;
  width: 2px;
  height: 32px;
  background-color: #6495ed;
  animation: cursorBlink 0.5s infinite;
}

@keyframes cursorBlink {
  49% {
    background-color: #6495ed;
  }
  50% {
    background-color: transparent;
  }
  99% {
    background-color: transparent;
  }
}

div.cursor.typing {
  animation: none;
}

h2 {
  color: #000000;
}

.school-logo {
  max-height: 3rem;
}
</style>
