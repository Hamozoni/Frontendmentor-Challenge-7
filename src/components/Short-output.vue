<template>
  <transition-group name="movin" class="output" tag="div">
    <div
      v-for="dataResulted in dataResult"
      :key="dataResulted.original_link"
      class="result"
    >
      <p class="link">{{ dataResulted.original_link }}</p>
      <p class="shorten">{{ dataResulted.full_short_link }}</p>
      <button
        v-if="this.copyed === 'copy'"
        @click="this.copyed = 'copied'"
        id="copy"
        :class="copyed"
      >
        Copy
      </button>
      <button v-else @click="this.copyed = 'copied'" id="copy" :class="copyed">
        Copied!
      </button>
    </div>
  </transition-group>
</template>

<script>
export default {
  name: "ShortOutput",
  data() {
    return {
      copyed: "copy",
    };
  },
  props: ["dataResult"],
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
.movin-enter-from,
.movin-leave-from {
  transform: rotatex(90deg);
  opacity: 0;
}
.movin-enter-active,
.movin-leave-active {
  transition: all 0.5s ease;
}
.movin-move {
  transition: all 0.5s ease;
}
</style>
