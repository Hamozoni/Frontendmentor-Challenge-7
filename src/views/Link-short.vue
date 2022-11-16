<template>
  <div class="link-shorten">
    <div class="container">
      <shorten-comp />
      <advanced-sta />
    </div>
  </div>
</template>

<script>
import ShortenComp from "@/components/ShortenComp.vue";
import AdvancedSta from "@/components/AdvancedSta.vue";
export default {
  name: "LinkShort",
  components: { ShortenComp, AdvancedSta },
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
