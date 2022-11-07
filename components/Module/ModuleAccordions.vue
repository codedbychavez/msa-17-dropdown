<template>
  <div class="module-container">
    <p>
      <button @click="toggleMode">
        {{ isAlwaysOpen ? "Turn on Single mode" : "Turn on Multi mode" }}
      </button>
    </p>

    <Accordion :key="computedAccordionKey" :isAlwaysOpen="isAlwaysOpen">
      <AccordionItem v-for="(accordion, index) in data.accordions" :key="index">
        <AccordionHeader>{{ accordion.title }}</AccordionHeader>
        <AccordionBody>{{ accordion.description }}</AccordionBody>
      </AccordionItem>
    </Accordion>
  </div>
</template>

<script>
import Accordion from "../Accordion/Accordion";
import AccordionItem from "../Accordion/AccordionItem";
import AccordionHeader from "../Accordion/AccordionHeader";
import AccordionBody from "../Accordion/AccordionBody";
// Accordion data
import accordionData from '../data/accordion.json'

export default {
  components: {
    Accordion,
    AccordionItem,
    AccordionHeader,
    AccordionBody,
  },
  data() {
    return {
      isAlwaysOpen: false,
      data: accordionData,
    };
  },
  methods: {
    toggleMode() {
      this.isAlwaysOpen = !this.isAlwaysOpen;
    },
  },
  computed: {
    computedAccordionKey() {
      let isAlwaysOpenProp = this.isAlwaysOpen;
      const isAlwaysOpenPropAsString = isAlwaysOpenProp.toString();
      return "accordionAlwaysOpen" + isAlwaysOpenPropAsString;
    },
  },
};
</script>

<style lang="scss">
.module-container {
  max-width: 866px;
  padding: 24px;
  margin: 0 auto;
}
</style>
