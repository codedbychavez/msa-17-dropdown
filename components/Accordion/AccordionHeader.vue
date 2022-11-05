<template>
  <CAccordionHeader>
    <slot />
  </CAccordionHeader>
</template>

<script>
import { CAccordionHeader } from "@coreui/vue";
export default {
  components: {
    CAccordionHeader,
  }
}
</script>

<style lang="scss">
  .accordion-button {
    background-color: #F1F1F1;
  }
</style>