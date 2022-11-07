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
