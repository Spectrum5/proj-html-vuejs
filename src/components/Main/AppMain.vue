<script>
import SliderMain from "../../components/Main/SliderMain.vue"
import TableMain from "../../components/Main/TableMain.vue"
import LifeStyleMain from "../../components/Main/LifeStyleMain.vue"
import BannerMain from "../../components/Main/BannerMain.vue"
import CardFeaturedMain from "../../components/Main/CardFeaturedMain.vue"
import YoutubeMain from "../../components/Main/YoutubeMain.vue"
import MainFooter from "../../components/Main/MainFooter.vue"


export default {
    components: {
        SliderMain,
        TableMain,
        LifeStyleMain,
        BannerMain,
        CardFeaturedMain,
        YoutubeMain,
        MainFooter,
    },
    data() {
        return {

        }
    }
}
</script>

<template>
    <!-- creazione template html -->
    <SliderMain />
    <TableMain />
    <LifeStyleMain />
    <BannerMain />
    <CardFeaturedMain />
    <YoutubeMain />
    <MainFooter />
</template>

<style scoped lang="scss">
/* aggiunta stile css */
</style>