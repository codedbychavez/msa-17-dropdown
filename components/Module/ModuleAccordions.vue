<template>
  <div class="module-container">
    <p>
      <button @click="toggleMode">
        {{ isAlwaysOpen ? "Turn on Single mode" : "Turn on Multi mode" }}
      </button>
    </p>

    <Accordion :key="computedAccordionKey" :isAlwaysOpen="isAlwaysOpen">
      <AccordionItem v-for="(accordion, index) in accordions" :key="index">
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

export default {
  components: {
    Accordion,
    AccordionItem,
    AccordionHeader,
    AccordionBody,
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
  data() {
    return {
      isAlwaysOpen: false,
      type: "ModuleAccordion",
      title: "Title goes here",
      description: "Some placeholder description",
      accordions: [
        {
          title: "Nisl elit, eget justo et imperdiet pharetra",
          description:
            "Consectetur tincidunt purus sit orci. Ultrices vulputate pharetra condimentum at eu arcu, ultricies euismod. Maecenas amet, diam erat cras. Amet, sit proin ut erat pharetra, dui interdum. Eget purus libero dapibus sit volutpat urna pretium. Cursus molestie nunc sit cras ipsum. Vel et scelerisque mattis aliquet scelerisque sit aliquam. Risus urna odio pellentesque nibh dolor, in viverra justo, erat. Habitant elit quisque semper dignissim quis fermentum euismod dui ornare. Elit eget enim, velit in sit. Nibh nec ipsum lectus eros, pretium hendrerit at sed in.",
        },
        {
          title: "Mauris, volutpat viverra vestibulum sit enim",
          description:
            "Consectetur tincidunt <b>purus sit orci</b>. Ultrices vulputate pharetra condimentum at eu arcu, ultricies euismod. Maecenas amet, diam erat cras. Amet, sit proin ut erat pharetra, dui interdum. Eget purus libero dapibus sit volutpat urna pretium. Cursus molestie nunc sit cras ipsum. Vel et scelerisque mattis aliquet scelerisque sit aliquam. Risus urna odio pellentesque nibh dolor, in viverra justo, erat. Habitant elit quisque semper dignissim quis fermentum euismod dui ornare. Elit eget enim, velit in sit. Nibh nec ipsum lectus eros, pretium hendrerit at sed in.",
        },
        {
          title: "Cursus risus, eget lobortis ultrices sit",
          description:
            "Eget ligula mauris magna scelerisque id. Fermentum purus, nulla cursus nibh cursus ut quam sed nec. Neque, eu, habitant eleifend facilisis interdum non. Feugiat ultricies ac feugiat a eget. Urna, risus pretium sit nisi diam purus.<br/></br>Consequat massa, quis enim nibh nisl et, vestibulum id. Nibh quis bibendum turpis viverra egestas vulputate sed vel, ac. Nulla turpis eu euismod ultricies mollis id duis. Convallis ipsum tellus ullamcorper nec aliquet vel duis arcu elementum. Congue fringilla condimentum sagittis ullamcorper facilisis commodo sit magnis.",
        },
        {
          title:
            "Vitae elit sem tincidunt proin scelerisque donec sit tristique",
          description:
            "Porta odio tortor at neque et neque, gravida. Egestas cursus erat id morbi cum scelerisque non. Vitae gravida integer vel nunc iaculis. Nulla est aliquet facilisis ullamcorper nisl, a, fames porta pellentesque.",
        },
      ],
    };
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
