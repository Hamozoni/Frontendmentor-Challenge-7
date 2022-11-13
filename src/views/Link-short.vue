<template>
  <div class="link-shorten">
    <div class="container">
      <shorten-comp />
      <short-output />
      <advanced-sta />
    </div>
  </div>
</template>

<script>
import ShortenComp from "@/components/ShortenComp.vue";
import ShortOutput from "@/components/Short-output.vue";
import AdvancedSta from "@/components/AdvancedSta.vue";
export default {
  name: "LinkShort",
  components: { ShortenComp, ShortOutput, AdvancedSta },
};
</script>

<style>
.link-shorten {
  margin-top: 180px;
  background-color: var(--bg-gray);
}
@media (min-width: 768px) {
  .link-shorten {
    margin-top: 120px;
  }
}
</style>
