<template>
  <div>
    <CAccordion class="accordion" :always-open="isAlwaysOpen" flush>
      <slot />
    </CAccordion>
  </div>
</template>

<script>
import { CAccordion } from "@coreui/vue";

export default {
  props: {
    isAlwaysOpen: Boolean,
  },
  components: {
    CAccordion,
  },
};
</script>