<script>
import AppHeader from "./components/AppHeader.vue";
import AppBanner from "./components/AppBanner.vue"
import AppMain from "./components/AppMain.vue";
import AppIcons from "./components/AppIcons.vue";
import AppFooter from "./components/AppFooter.vue";




export default{
    components: {
      AppHeader,
      AppBanner,
      AppMain,
      AppIcons,
      AppFooter
    },
    data(){
      return{
        // bannerImage: "../assets/img/banner.jpeg"
      }
    }
}
</script>


<template>
    <AppHeader/>
    <!-- <AppBanner
      :bannerImage= "bannerImage"
    /> -->
    <AppBanner/>
    <AppMain/>
    <AppIcons/>
    <AppFooter/>
</template>

<style lang="scss">



</style>