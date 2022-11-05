<template>
  <CAccordionItem>
    <slot />
  </CAccordionItem>
</template>

<script>
import { CAccordionItem } from '@coreui/vue'

export default {
  components: {
    CAccordionItem,
  }
}
</script>