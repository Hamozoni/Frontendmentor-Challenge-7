<template>
  <div class="input">
    <input
      v-model="linkInPut"
      type="text"
      id="shortLink"
      :class="emty && 'emty'"
      placeholder="Shorten a Link Here..."
    />
    <label v-if="emty" for="shortLink">please add a link</label>
    <button @click="fecthing" id="shortBtn">Shorten it!</button>
  </div>
  <transition name="apear">
    <short-output v-if="resuShow" :dataResult="resu" />
  </transition>
</template>

<script>
import ShortOutput from "@/components/Short-output.vue";
export default {
  name: "ShortenComp",
  components: { ShortOutput },
  data() {
    return {
      resu: [],
      linkInPut: "",
      resuShow: false,
      emty: false,
    };
  },
  methods: {
    fecthing() {
      if (this.linkInPut) {
        fetch(`https://api.shrtco.de/v2/shorten?url=${this.linkInPut}`)
          .then((respounse) => respounse.json())
          .then((data) => {
            this.resu.unshift(data.result);
            this.resuShow = true;
            this.emty = false;
          });
        this.linkInPut = "";
      } else {
        this.emty = true;
      }
    },
  },
};
</script>

<style scoped>
.input {
  position: relative;
  transform: translateY(-50%);
  width: 100%;
  padding: 40px;
  background-image: url(@/assets/bg-shorten-desktop.svg);
  background-color: var(--very-dark-blue);
  background-size: cover;
  border-radius: 10px;
  margin-bottom: -70px;
}
.input #shortLink {
  padding: 20px;
  border-radius: 10px;
  width: 100%;
}
.input #shortLink.emty {
  border: 2px solid red;
}
.input #shortLink.emty::placeholder {
  color: red;
}
.input #shortBtn {
  width: 100%;
  padding: 17px 0;
  background-color: var(--cyan);
  color: #fff;
  border-radius: 10px;
  margin-top: 30px;
}
.input label {
  position: absolute;
  left: 50px;
  top: 105px;
  color: red;
}
@media (min-width: 768px) {
  .input {
    display: flex;
    align-items: center;
    justify-content: space-between;
    gap: 20px;
  }
  .input #shortLink {
    width: calc(80% - 15px);
    margin-right: 30px;
  }
  .input #shortBtn {
    width: calc(20% - 15px);
    margin-top: 0;
  }
}
.apear-enter-from,
.apear-leave-from {
  transform: rotatex(90deg);
  opacity: 0;
}
.apear-enter-active,
.apear-leave-active {
  transition: all 0.5s ease;
}
</style>
