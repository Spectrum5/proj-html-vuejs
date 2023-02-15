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
            step: '',
            transitioning: false
        }
    },
    mounted() {
        this.setStep()
        this.resetTranslate()
    },
    methods: {
        setStep() {
            const innerWidth = this.$refs.inner.scrollWidth
            const totalCards = this.cards.length
            this.step = `${innerWidth / totalCards}px`
        },
        next() {
            if (this.transitioning) return
            this.transitioning = true
            this.moveLeft()
            this.afterTransition(() => {
                const card = this.cards.shift()
                this.cards.push(card)
                this.resetTranslate()
                this.transitioning = false
            })
        },
        prev() {
            if (this.transitioning) return
            this.transitioning = true
            this.moveRight()
            this.afterTransition(() => {
                const card = this.cards.pop()
                this.cards.unshift(card)
                this.resetTranslate()
                this.transitioning = false
            })
        },
        moveLeft() {
            this.innerStyles = {
                transform: `translateX(-${this.step})
                    translateX(-${this.step})`
            }
        },
        moveRight() {
            this.innerStyles = {
                transform: `translateX(${this.step})
                    translateX(-${this.step})`
            }
        },
        afterTransition(callback) {
            const listener = () => {
                callback()
                this.$refs.inner.removeEventListener('transitionend', listener)
            }
            this.$refs.inner.addEventListener('transitionend', listener)
        },
        resetTranslate() {
            this.innerStyles = {
                transition: 'none',
                transform: `translateX(-${this.step})`
            }
        }
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
                                    <p class="card-text">{{ card.description }}</p>
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
}

.inner {
    transition: transform 1s;
    white-space: nowrap;
}

.card {
    width: calc(100% / 3 + 15px);
    display: inline-flex;
}

/* optional */
button {
    margin-right: 5px;
    margin-top: 10px;
}
</style>