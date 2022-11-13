<template>
  <div class="advanced">
    <div class="head">
      <h2>Advanced Statistics</h2>
      <p>
        Track how your links are performing across the web with our advanced
        statistics dashboard
      </p>
    </div>
    <div class="features">
      <div class="feat-box">
        <div class="img">
          <img src="@/assets/icon-brand-recognition.svg" alt="brand" />
        </div>
        <h3>Brand Recognition</h3>
        <p>
          Boost your brand recognition with each click. Generic links don’t mean
          a thing. Branded links help instil confidence in your content.
        </p>
      </div>
      <div class="feat-box">
        <div class="img">
          <img src="@/assets/icon-detailed-records.svg" alt="brand" />
        </div>
        <h3>Detailed Records</h3>
        <p>
          Gain insights into who is clicking your links. Knowing when and where
          people engage with your content helps inform better decisions.
        </p>
      </div>
      <div class="feat-box">
        <div class="img">
          <img src="@/assets/icon-fully-customizable.svg" alt="brand" />
        </div>
        <h3>Fully Customizable</h3>
        <p>
          Improve brand awareness and content discoverability through
          customizable links, supercharging audience engagement.
        </p>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  name: "AdvancedSta",
};
</script>

<style>
.advanced {
  margin-top: 100px;
  padding-bottom: 150px;
}
.advanced .head {
  text-align: center;
  margin: 0 auto 40px;
  width: 530px;
  max-width: 100%;
}
.advanced .head h2 {
  font-size: 22px;
  color: var(--very-dark-violet);
  margin-bottom: 20px;
}
.advanced .head p {
  color: var(--grayish-violet);
}
.advanced .features .feat-box {
  position: relative;
  text-align: center;
  background-color: var(--weight);
  padding: 20px;
  border-radius: 5px;
  margin-top: 60px;
}
.advanced .features .feat-box:nth-child(1)::before {
  content: "";
  position: absolute;
  width: 8px;
  height: 200%;
  background-color: var(--cyan);
  left: 50%;
  top: 100%;
}
.advanced .features .feat-box .img {
  text-align: center;
  width: 70px;
  height: 70px;
  position: relative;
  top: -50px;
  left: 50%;
  transform: translateX(-50%);
  margin-bottom: -50px;
  padding: 10px;
  background-color: var(--dark-violet);
  border-radius: 50%;
}
.advanced .features .feat-box h3 {
  color: var(--very-dark-violet);
  margin: 15px 0;
}
.advanced .features .feat-box p {
  color: var(--grayish-violet);
}
@media (min-width: 992px) {
  .advanced .head h2 {
    font-size: 38px;
  }
  .advanced .features {
    display: flex;
    gap: 40px;
  }
  .advanced .features .feat-box {
    margin-top: 0;
    text-align: unset;
  }
  .advanced .features .feat-box .img {
    left: 20%;
  }
  .advanced .features .feat-box:nth-child(2) {
    left: 0;
    top: 40px;
  }
  .advanced .features .feat-box:nth-child(1)::before {
    width: 200%;
    height: 8px;
    left: 100%;
    top: 60%;
  }
  .advanced .features .feat-box:nth-child(3) {
    left: 0;
    top: 80px;
  }
  .advanced .features .feat-box .img {
    text-align: center;
    width: 70px;
    height: 70px;
    position: relative;
    top: -50px;
    margin-bottom: -50px;
    padding: 10px;
    background-color: var(--dark-violet);
    border-radius: 50%;
  }
  .advanced .features .feat-box h3 {
    color: var(--very-dark-violet);
    margin: 15px 0;
  }
  .advanced .features .feat-box p {
    color: var(--grayish-violet);
  }
}
</style>
