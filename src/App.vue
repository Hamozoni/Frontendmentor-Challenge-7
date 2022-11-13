<template>
  <div id="app">
    <Header-comp />
    <Landing-comp />
    <link-short />
    <Boost-comp />
    <Footer-comp />
  </div>
</template>
<script>
import HeaderComp from "./views/Header.vue";
import LandingComp from "./views/Landing.vue";
import LinkShort from "./views/Link-short.vue";
import BoostComp from "@/components/boost.vue";
import FooterComp from "./views/Footer.vue";
export default {
  components: { HeaderComp, LandingComp, LinkShort, BoostComp, FooterComp },
};
</script>
<style>
:root {
  --weight: #fff;
  --cyan: hsl(180, 66%, 49%);
  --dark-violet: hsl(257, 27%, 26%);
  --red: hsl(0, 87%, 67%);
  --gray: hsl(0, 0%, 75%);
  --grayish-violet: hsl(257, 7%, 63%);
  --very-dark-blue: hsl(255, 11%, 22%);
  --very-dark-violet: hsl(260, 8%, 14%);
  --bg-gray: hsl(225deg 33% 95%);
  --font-size: 18px;
}
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  transition: all 0.3s;
}
li {
  list-style: none;
  font-size: var(--font-size);
  font-weight: 500;
}
a {
  text-decoration: none;
  font-size: var(--font-size);
  font-weight: 500;
}
p {
  font-size: var(--font-size);
}
img,
picture {
  max-width: 100%;
}
button {
  cursor: pointer;
  user-select: none;
  border: none;
  outline: none;
  font-size: var(--font-size);
  font-weight: 500;
}
input {
  border: none;
  outline: none;
}
body {
  font-family: "Poppins", sans-serif;
}
#app {
  overflow: hidden;
}
.container {
  margin: 0 auto;
  padding: 0 15px;
  max-width: 100%;
}
@media (min-width: 768px) {
  .container {
    width: 750px;
  }
}
@media (min-width: 992px) {
  .container {
    width: 970px;
  }
}
@media (min-width: 1200px) {
  .container {
    width: 1170px;
  }
}
</style>
