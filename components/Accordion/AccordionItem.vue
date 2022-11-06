<template>
  <CAccordionItem class="accordion-item">
    <slot />
  </CAccordionItem>
</template>

<script>
import { CAccordionItem } from "@coreui/vue";

export default {
  components: {
    CAccordionItem,
  },
};
</script>

<style lang="scss">
.accordion-item {
  background-color: #f1f1f1;
  margin-bottom: 32px;
  border: 0;
  max-width: 866px;
}
</style>
