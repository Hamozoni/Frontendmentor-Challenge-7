<template>
  <div class="input">
    <input type="text" id="shortLink" placeholder="Shorten a link here..." />
    <button id="shortBtn">Shorten it!</button>
  </div>
</template>

<script>
export default {
  name: "ShortenComp",
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
.input #shortBtn {
  width: 100%;
  padding: 17px 0;
  background-color: var(--cyan);
  color: #fff;
  border-radius: 10px;
  margin-top: 30px;
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
</style>
