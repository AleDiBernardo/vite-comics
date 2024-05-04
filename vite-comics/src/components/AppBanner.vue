<script>
export default {
    props: {
        bannerImage: String
    }
};
</script>

<template>
    <!-- ? Why it doesn't work? -->
    <!-- <section class="banner" :style="{'background-image': `url(${bannerImage});`}"></section> -->
    <section class="banner"></section>

</template>
<style scoped lang="scss">
@use "./style/partials/variables" as *;
@use "./style/partials/mixins" as *;

.banner {
    height: 400px;
    background-image: url('../assets/img/banner.avif');
    background-size: cover;
    background-repeat: no-repeat;
}

</style>
