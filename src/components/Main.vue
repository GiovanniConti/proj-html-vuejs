<template>
  <main>
    <SectionBoxes></SectionBoxes>
    <WorkingProcess></WorkingProcess>
    <WorkWithUs></WorkWithUs>
    <BlogHighlights></BlogHighlights>
  </main>
</template>

<script>
import SectionBoxes from "./SectionBoxes.vue";
import WorkingProcess from "./WorkingProcess.vue";
import WorkWithUs from "./WorkWithUs.vue";
import BlogHighlights from "./BlogHighlights.vue";

export default {
  name: "Main",
  components: {
    SectionBoxes,
    WorkingProcess,
    WorkWithUs,
    BlogHighlights,
  },
  props: {

  },
  data() {
    return {

    };
  },
}
</script>

<style>

</style>