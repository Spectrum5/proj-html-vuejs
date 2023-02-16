<script>
export default {
    data() {
        return {
            cards: [
                {
                    image: new URL("../../assets/img/anime-fashion.webp", import.meta.url).href,
                    title: "Live Ideas You Might Be Anime",
                    text: 'December 26, 2022',
                    description: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Maxime nesciunt fugiat aut natus sapiente atque!",
                    link: "#"
                },
                {
                    image: new URL("../../assets/img/visit-france.webp", import.meta.url).href,
                    title: "Reasons To Visit France",
                    text: 'December 26, 2022',
                    description: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Maxime nesciunt fugiat aut natus sapiente atque!",
                    link: "#nogo"
                },
                {
                    image: new URL("../../assets/img/travel-alone.webp", import.meta.url).href,
                    title: "Traveling Alone is Awesome",
                    text: 'December 26, 2022',
                    description: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Maxime nesciunt fugiat aut natus sapiente atque!",
                    link: "#nogo"
                },
                {
                    image: new URL("../../assets/img/best-places.webp", import.meta.url).href,
                    title: "Best Places For A Road Trip",
                    text: 'December 26, 2022',
                    description: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Maxime nesciunt fugiat aut natus sapiente atque!",
                    link: "#nogo"
                },
                {
                    image: new URL("../../assets/img/rice-ball.webp", import.meta.url).href,
                    title: "Rice Ball",
                    text: 'December 26, 2022',
                    description: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Maxime nesciunt fugiat aut natus sapiente atque!",
                    link: "#nogo"
                },
                {
                    image: new URL("../../assets/img/winter.webp", import.meta.url).href,
                    title: "The Winter Is Coming",
                    text: 'December 26, 2022',
                    description: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Maxime nesciunt fugiat aut natus sapiente atque!",
                    link: "#nogo"
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
            if (this.step === this.cards.length - 3) {
                this.step = -1
            }
            this.$refs.inner.style.transform = `translateX(-${(100 / 3) * ++this.step}%)`
        },
        prev() {
            if (this.step === 0) {
                this.step = this.cards.length - 4
                this.$refs.inner.style.transform = `translateX(-${(100 / 3) * ++this.step}%)`
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
        <div class="container">
            <div class="row">
                <div class="col-6 pt-5">
                    <h5 class="text-uppercase fs-4 fw-bold ">
                        featured posts
                    </h5>
                </div>
                <div class="col-6 d-flex pt-5 justify-content-end">
                    <button class="carousel-btn left" @click="prev"><font-awesome-icon icon="fa-solid fa-chevron-left"/></button>
                    <button class="carousel-btn right" @click="next"><font-awesome-icon icon="fa-solid fa-chevron-right"/></button>
                </div>
            </div>
        </div>
    </section>
    <section>
        <div class="container">
            <div class="row">
                <div class="col">
                    <div class="carousel">
                        <div class="inner" ref="inner" :style="innerStyles">
                            <div class="card" v-for="(card, index) in cards" :key="index">
                                <img :src="card.image" class="card-img-top" alt="card image">
                                <div class="card-body">
                                    <h5 class="card-title fs-6 fw-bold">{{ card.title }}</h5>
                                    <p class="card-text">{{ card.text }}</p>
                                    <p class="">{{ card.description }}</p>
                                    <a :href="card.link" class="btn btn-primary">Read More</a>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>
</template>

<style lang="scss" scoped>
/* aggiunta stile css */
@use '../../styles/partials/variables.scss' as*;
.carousel {
    width: 100%;
    overflow: hidden;
    text-align: center;

    .inner {
        display: flex;
        transition: all 500ms ease-in-out;
    }

    .card {
        flex-basis: calc(100% / 3 - 4px);
        flex-shrink: 0;
        margin: 2px;
        color: $text_dark;
    }
    .card-text {
        font-size: 0.9rem;
        color: $text_light;
    }
}
.carousel-btn {
        width: 35px;
        height: 35px;
        border-radius: 50%;
        background-color: $background_dark;
        color: $text_white;
        font-weight: bold;
        border: none;
        outline: none;
        font-size: 1.3rem;
        margin-left: 20px;

        &:hover {
            background-color: $background_red;
        }
    }

    .btn-primary {
        background-color: $background_red;
        border: none;
        padding: 5px 30px 5px 30px;
        border-radius: 50px;
        &:hover {
            background-color: $background_dark;
        }
    }
</style>