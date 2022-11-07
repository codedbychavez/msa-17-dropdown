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

<style lang="scss">

.accordion-item {
  background-color: #f1f1f1;
  margin-bottom: 32px;
  border: 0;
  max-width: 866px;
}

.accordion-button {
  background-color: #f1f1f1;
  border: 0;
  &:not(.collapsed) {
    box-shadow: none;
    background-color: transparent;
  }
  &::after {
    width: 12px;
    height: 12px;
    background-size: 12px;
  }
}

</style>
