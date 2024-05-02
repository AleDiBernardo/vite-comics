<script>
import AppHeader from "./components/AppHeader.vue";
import AppMain from "./components/AppMain.vue";
import AppIcons from "./components/AppIcons.vue";
import AppFooter from "./components/AppFooter.vue";




export default{
    components: {
      AppHeader,
      AppMain,
      AppIcons,
      AppFooter
    },
    data(){
      return{
        
      }
    }
}
</script>


<template>
    <AppHeader/>
    <AppMain/>
    <AppIcons/>
    <AppFooter/>
</template>

<style lang="scss">

body {
  background-color: lightcoral;
  color: white;
  font-family: monospace;
}

.container {
  width: 70%;
  margin: 0 auto;
  padding: 1rem 0;

}

</style>