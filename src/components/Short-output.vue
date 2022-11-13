<template>
  <div class="output">
    <div class="result">
      <p class="link">https://www.google.com/search?q</p>
      <p class="shorten">https://www.google.com</p>
      <button id="copy">Copy</button>
    </div>
    <div class="result">
      <p class="link">https://www.google.com/search?q</p>
      <p class="shorten">https://www.google.com</p>
      <button id="copy" class="copied">Copied!</button>
    </div>
    <div class="result">
      <p class="link">https://www.google.com/search?q</p>
      <p class="shorten">https://www.google.com</p>
      <button id="copy">Copy</button>
    </div>
  </div>
</template>

<script>
export default {
  name: "ShortOutput",
};
</script>

<style>
.output {
  margin-top: 20px;
}
.output .result {
  background: #fff;
  border-radius: 8px;
  margin-bottom: 30px;
}
.output .result .link {
  padding: 15px;
  border-bottom: 1px solid var(--gray);
}
.output .result .shorten {
  color: var(--cyan);
  padding: 15px;
}
.output .result #copy {
  background-color: var(--cyan);
  color: #fff;
  padding: 10px 25px;
  margin: 15px;
  border-radius: 5px;
  width: calc(100% - 30px);
}
.output .result #copy.copied {
  background-color: var(--dark-violet);
}
@media (min-width: 768px) {
  .output .result {
    display: flex;
    justify-content: space-between;
    align-items: center;
    gap: 20px;
    padding: 15px 30px;
  }
  .output .result .link {
    padding: 0;
    border-bottom: none;
  }
  .output .result #copy {
    width: fit-content;
    margin: 0;
  }
  .output .result .shorten {
    padding: 0;
    text-align: end;
    flex: 1;
  }
}
</style>
