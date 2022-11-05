<template>
  <div>
    <CAccordion :always-open="isAlwaysOpen">
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

<style>
/* TODO: Hide and show this component */
</style>