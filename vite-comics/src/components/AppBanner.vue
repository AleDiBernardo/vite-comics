<script>
export default {
    props: {
        // bannerImage: String
    }
};
</script>

<template>
    <!-- ? Why it doesn't work? -->
    <!-- <section class="banner" :style="{'background-image': `url(../assets/img/${bannerImage});`}"></section> -->
    <section class="banner"></section>

</template>
<style scoped lang="scss">

.banner {
    height: 500px;
    background-position: center;
    background-image: url('../assets/img/banner.avif');
    background-size: cover;
    background-repeat: no-repeat;
}

</style>
