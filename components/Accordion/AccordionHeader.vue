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
  },
};
</script>

<style lang="scss">
// The accordion-button is in the header
.accordion-button {
  background-color: #f1f1f1;
  color: #1b1464;
  border: 0;
  &:not(.collapsed) {
    box-shadow: none;
    // Sets the active background color of the button
    background-color: transparent;
    // Sets the color of the active/expanded accordion
    color: #1b1464;
  }
  &::after {
    width: 12px;
    height: 12px;
    background-size: 12px;
  }
}
</style>
