<script>
export default {
    data() {
        return {
            cards: [
                {
                    image: new URL("../../assets/img/best-places.webp", import.meta.url).href,
                    title: "Live Ideas You Might Be Anime",
                    text: 'December 26, 2022',
                    description: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Maxime nesciunt fugiat aut natus sapiente atque!",
                    link: "#"
                },
                {
                    image: new URL("../../assets/img/best-places.webp", import.meta.url).href,
                    title: "Card Title 2",
                    text: 'December 26, 2022',
                    description: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Maxime nesciunt fugiat aut natus sapiente atque!",
                    link: "#"
                },
                {
                    image: new URL("../../assets/img/best-places.webp", import.meta.url).href,
                    title: "Card Title 3",
                    text: 'December 26, 2022',
                    description: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Maxime nesciunt fugiat aut natus sapiente atque!",
                    link: "#"
                },
                {
                    image: new URL("../../assets/img/best-places.webp", import.meta.url).href,
                    title: "Card Title 4",
                    text: 'December 26, 2022',
                    description: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Maxime nesciunt fugiat aut natus sapiente atque!",
                    link: "#"
                },
                {
                    image: new URL("../../assets/img/best-places.webp", import.meta.url).href,
                    title: "Card Title 5",
                    text: 'December 26, 2022',
                    description: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Maxime nesciunt fugiat aut natus sapiente atque!",
                    link: "#"
                },
                {
                    image: new URL("../../assets/img/best-places.webp", import.meta.url).href,
                    title: "Card Title 6",
                    text: 'December 26, 2022',
                    description: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Maxime nesciunt fugiat aut natus sapiente atque!",
                    link: "#"
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
                <div class="col-6">
                    <div>
                        <h2>Portfolio</h2>
                    </div>
                </div>
                <div class="col-6 d-flex justify-content-end">
                    <button @click="prev">prev</button>
                    <button @click="next">next</button>
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
                                    <h5 class="card-title">{{ card.title }}</h5>
                                    <p class="card-text smaller">{{ card.text }}</p>
                                    <p class="card-text smaller">{{ card.description }}</p>
                                    

                                    <a :href="card.link" class="btn btn-primary">Go somewhere</a>
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
.carousel {
    width: 100%;
    overflow: hidden;
    text-align: center;

    .inner {
        display: flex;
        transition: all 500ms ease-in-out;
    }

    .card {
        flex-basis: calc(100% / 3);
        flex-shrink: 0;
    }
}
</style>