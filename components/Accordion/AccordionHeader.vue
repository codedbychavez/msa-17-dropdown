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