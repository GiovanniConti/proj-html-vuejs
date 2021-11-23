<template>
  <main>
    <SectionBoxes></SectionBoxes>
    <WorkingProcess></WorkingProcess>
    <WorkWithUs></WorkWithUs>
  </main>
</template>

<script>
import SectionBoxes from "./SectionBoxes.vue";
import WorkingProcess from "./WorkingProcess.vue";
import WorkWithUs from "./WorkWithUs.vue";

export default {
  name: "Main",
  components: {
    SectionBoxes,
    WorkingProcess,
    WorkWithUs,
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