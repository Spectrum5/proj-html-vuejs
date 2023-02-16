<script>








export default {
    data() {
        return {
            cards: [
                {
                    image: new URL("../../assets/img/healthy-foods.webp", import.meta.url).href,
                    title: 'The best Healthy Foods in 2022',
                    text: 'December 26, 2022',
                },
                {
                    image: new URL("../../assets/img/winter.webp", import.meta.url).href,
                    title: 'The Best Winter Outfits',
                    text: 'December 26, 2022',
                },
                {
                    image: new URL("../../assets/img/photographers-mistakes.webp", import.meta.url).href,
                    title: 'Beginner Photographers Mistake',
                    text: 'December 26, 2022',
                },
                {
                    image: new URL("../../assets/img/anime-fashion.webp", import.meta.url).href,
                    title: 'Live Ideas You Might Be Anime',
                    text: 'December 26, 2022'
                },
                {
                    image: new URL("../../assets/img/rice-ball.webp", import.meta.url).href,
                    title: "Card Title 5",
                    text: 'December 26, 2022',
                },
                {
                    image: new URL("../../assets/img/best-places.webp", import.meta.url).href,
                    title: "Card Title 6",
                    text: 'December 26, 2022',
                },
                {
                    image: new URL("../../assets/img/travel-alone.webp", import.meta.url).href,
                    title: "Card Title 6",
                    text: 'December 26, 2022',
                },

                // add more cards here
            ],
            innerStyles: {},
            step: 0,
            transitioning: false
        }
    },

    methods: {

        next() {
            if (this.step === this.cards.length - 4) {
                this.step = -1
            }
            this.$refs.inner.style.transform = `translateX(-${(100 / 4) * ++this.step}%)`
        },
        prev() {
            if (this.step === 0) {
                this.step = this.cards.length - 5
                this.$refs.inner.style.transform = `translateX(-${(100 / 4) * ++this.step}%)`
            }
            else {
                this.step -= 2
                this.next()
            }
        },
    },
    name: 'Carousel',
    components: {
    }
}
</script>

<template>
    <section>
        <div class="container-fluid">
            <div class="row">
                <div class="col">
                    <div class="carousel-container">
                        <div class="carousel">
                            <div class="inner" ref="inner" :style="innerStyles">
                                <div class="card" v-for="(card, index) in cards" :key="index">
                                    <img :src="card.image" class="card-img-top" alt="card image">
                                    <div class="card-body">
                                        <h5 class="card-title fs-6 fw-bold">{{ card.title }}</h5>
                                        <p class="card-text fw-bold">{{ card.text }}</p>
                                    </div>
                                </div>
                            </div>
                        </div>
                        <button class="carousel-btn left" @click="prev">prev</button>
                        <button class="carousel-btn right" @click="next">next</button>
                    </div>
                </div>
            </div>
        </div>
</section>
</template>

<style lang="scss" scoped>
/* aggiunta stile css */
@use '../../styles/partials/variables.scss' as*;

.container-fluid {
    background-color: $background_light;
    padding: 20px;
}

.carousel-container {
    position: relative;

    .carousel {
        width: 100%;
        overflow: hidden;
        text-align: center;

        .inner {
            display: flex;
            transition: all 500ms ease-in-out;

            .card {
                flex-basis: calc(100% / 4);
                flex-shrink: 0;
                margin: 2px;

                .card-body {
                    color: $text_dark;

                    .card-text {
                        font-size: 0.9rem;
                        color: $text_light;
                    }

                }
            }
        }
    }

    .carousel-btn {
        position: absolute;
        top: 50%;
        transform: translateY(-50%);
        width: 50px;
        height: 50px;
        border-radius: 50%;
        background-color: #fff;
        color: #000;
        font-weight: bold;
        border: none;
        outline: none;
    }

    .carousel-btn.left {
        left: 20px;
    }

    .carousel-btn.right {
        right: 20px;
    }
}
</style>