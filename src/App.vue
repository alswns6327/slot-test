<template>
  <!-- <SolotTest></SolotTest> -->
    <!-- <ScopedSlot></ScopedSlot> -->
    <a v-for="tab in tabs" :key="tab.id" :style="{color : (tab.id === currentTab ? 'blue' : 'red')}"
      @click="changeTab(tab.id)"
    >{{ tab.label }}</a>
    <br/>
    <component :is="currentTab"></component>
    
</template>

<script>
import Coral from './components/Coral.vue';
import Midway from './components/Midway.vue';
import LeyteGulf from './components/LeyteGulf.vue';
import ScopedSlot from './components/ScopedSlot.vue';
import SolotTest from './components/SolotTest.vue';

  export default{
    name: "App",
    components: { SolotTest, ScopedSlot, "A" : Coral, "B" :Midway, "C" : LeyteGulf },
    data(){
      return {
        currentTab : 'B',
        tabs : [
          {id : "A", label : "Coral"},
          {id : "B", label : "Midway"},
          {id : "C", label : "LeyteGulf"},
        ]
      }
    },
    methods : {
      changeTab(id){
        this.currentTab = id;
      }
    }
}
  
</script>
<style scoped>
</style>
