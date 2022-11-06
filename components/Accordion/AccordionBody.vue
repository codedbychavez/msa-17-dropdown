<template>
  <CAccordionBody>
    <slot />
  </CAccordionBody>
</template>

<script>
import { CAccordionBody } from "@coreui/vue";

export default {
  components: {
    CAccordionBody,
  },
};
</script>
