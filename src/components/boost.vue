<template>
  <section class="boost">
    <h3>Boost your links today</h3>
    <button id="boostBtn">Get Started</button>
  </section>
</template>

<script>
export default {
  name: "boostComp",
};
</script>

<style>
.boost {
  text-align: center;
  background-color: var(--very-dark-blue);
  background-image: url(@/assets/bg-boost-desktop.svg);
  background-position: center;
  padding: 50px 20px;
}
.boost h3 {
  color: var(--weight);
  font-size: 32px;
  margin-bottom: 20px;
}
.boost #boostBtn {
  color: var(--weight);
  background-color: var(--cyan);
  padding: 15px 40px;
  border-radius: 30px;
}
</style>
