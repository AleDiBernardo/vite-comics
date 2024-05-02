<script>
import AppHeader from "./components/AppHeader.vue";
import AppMain from "./components/AppMain.vue";


export default{
    components: {
      AppHeader,
      AppMain
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
</template>

<style lang="scss">

body {
  background-color: lightcoral;
  color: white;
}

.container {
  width: 70%;
  margin: 0 auto;
  padding: 1.5rem 0;

}

</style>