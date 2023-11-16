<template>
  <!-- <SolotTest></SolotTest> -->
    <ScopedSlot></ScopedSlot>
</template>

<script>
import ScopedSlot from './components/ScopedSlot.vue';
import SolotTest from './components/SolotTest.vue';

  export default{
    name: "App",
    components: { SolotTest, ScopedSlot }
}
  
</script>
<style scoped>
</style>
