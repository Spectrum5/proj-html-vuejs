<script>



export default {
    data() {
        return {
            cards: [
                {
                    image: new URL("../../assets/img/anime-fashion.webp", import.meta.url).href,
                    title: "FASHION",
                },
                {
                    image: new URL("../../assets/img/success-story.webp", import.meta.url).href,
                    title: "CULTURE",
                },
                {
                    image: new URL("../../assets/img/healthy-foods.webp", import.meta.url).href,
                    title: "FOOD",
                },
                {
                    image: new URL("../../assets/img/visit-france.webp", import.meta.url).href,
                    title: "LIFESTYLE",
                },
                {
                    image: new URL("../../assets/img/travel-alone.webp", import.meta.url).href,
                    title: "STORIES",
                },
                {
                    image: new URL("../../assets/img/best-places.webp", import.meta.url).href,
                    title: "TRAVEL",
                },
                // add more cards here
            ],

        }
    }
}
</script>

<template>
<!-- creazione template html -->
    <div class="container-fluid">
        <div class="row row-cols-6 mt-4">
            <div class="col" v-for="element in cards">
                <div class="position-relative filter">
                    <img class="w-100 rounded " :src="element.image" alt="Anime Fashion">
                    <h4 class="position-absolute start-50 top-50 translate-middle">
                        {{ element.title }}
                    </h4>
                </div>
            </div>
        </div>
</div>
</template>

<style scoped lang="scss">
/* aggiunta stile css */
@use '../../styles/partials/variables.scss' as*;

.filter {
    img {
        filter:brightness(0.5)
    }
    &:hover img {
        filter: brightness(1)
    }
    h4 {
        color: $text_white;
        font-weight: 900;
    }
    &:hover h4 {
        color: $text_dark;
    }
}


</style>