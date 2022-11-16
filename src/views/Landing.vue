<template>
  <main role="content" class="landing">
    <div class="container">
      <div class="right">
        <img src="../assets/illustration-working.svg" alt="illustration" />
      </div>
      <div class="left">
        <h1 class="lan-head">More than just shorterlinks</h1>
        <p class="lan-pra">
          Build your brand's recognition and get detailed insights on how your
          links are performing
        </p>
        <button id="landStart">Get Started</button>
      </div>
    </div>
  </main>
</template>

<script>
export default {
  name: "LandingComp",
};
</script>

<style>
.landing {
  margin: 0 50px;
}
.container .right {
  position: relative;
  transform: translateX(30%);
}
.container .right img {
  width: 120%;
}
.container .left .lan-head {
  font-size: 32px;
  font-weight: bold;
  color: var(--very-dark-blue);
}
.container .left .lan-pra {
  color: var(--grayish-violet);
  margin: 30px 0;
}
#landStart {
  padding: 15px 35px;
  border-radius: 30px;
  background-color: var(--cyan);
  color: #fff;
}
.container .left {
  text-align: center;
  margin-top: 40px;
}
@media (min-width: 992px) {
  .landing .container {
    display: flex;
    flex-direction: row-reverse;
    align-items: center;
    gap: 15px;
  }
  .container .left {
    flex-basis: 40%;
    text-align: unset;
    margin-top: 0;
  }
  .container .right {
    flex-basis: 60%;
  }
  .container .left .lan-head {
    line-height: 1.2;
    font-size: 53px;
  }
  .container .left .lan-pra {
    width: 85%;
  }
}
</style>
