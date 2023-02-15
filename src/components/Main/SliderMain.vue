<script>
import CardTopSlider from './OtherComponents/CardTopSlider.vue';
export default {
    components: {
        CardTopSlider,
    },
    data() {
        return {
            sliderCards: [
                {
                    img: '../../src/assets/img/healthy-foods.webp',
                    title: 'The best Healthy Foods in 2022',
                    text: 'December 26, 2022'
                },
                {
                    img: '../../src/assets/img/winter.webp',
                    title: 'The Best Winter Outfits',
                    text: 'December 26, 2022'
                },
                {
                    img: '../../src/assets/img/photographers-mistakes.webp',
                    title: 'Beginner Photographers Mistake',
                    text: 'December 26, 2022'
                },
                {
                    img: '../../src/assets/img/best-places.webp',
                    title: 'Live Ideas You Might Be Anime',
                    text: 'December 26, 2022'
                },

            ]
        }
    }
}
</script>

<template>
    <!-- creazione template html -->
    <div class="container-fluid">
        <div class="row">
            <div class="slider col-12">
                <div class="cards d-flex flex-wrap">
                    <CardTopSlider :sliderCards="sliderCards" />
                </div>
            </div>
        </div>
    </div>
</template>

<style scoped lang="scss">
/* aggiunta stile css */
@use '../../styles/partials/variables.scss' as*;

.container-fluid {
    background-color: $background_light;
    padding: 20px;
}
</style>