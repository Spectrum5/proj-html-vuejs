<script>
export default {
    data() {
        return {
            currentSlide: 0,
            cards: [
                {
                    title: 'Card title 1',
                    body: 'Some quick example text to build on the card title and make up the bulk of the card\'s content.',
                    imageUrl: '../../assets/img/best-places.webp',
                    altText: '...'
                },
                {
                    title: 'Card title 2',
                    body: 'Some quick example text to build on the card title and make up the bulk of the card\'s content.',
                    imageUrl: '../../assets/img/best-places.webp',
                    altText: '...'
                },
                {
                    title: 'Card title 3',
                    body: 'Some quick example text to build on the card title and make up the bulk of the card\'s content.',
                    imageUrl: '../../assets/img/best-places.webp',
                    altText: '...'
                },
                {
                    title: 'Card title 3',
                    body: 'Some quick example text to build on the card title and make up the bulk of the card\'s content.',
                    imageUrl: '../../assets/img/best-places.webp',
                    altText: '...'
                },
                {
                    title: 'Card title 3',
                    body: 'Some quick example text to build on the card title and make up the bulk of the card\'s content.',
                    imageUrl: '../../assets/img/best-places.webp',
                    altText: '...'
                },
                {
                    title: 'Card title 3',
                    body: 'Some quick example text to build on the card title and make up the bulk of the card\'s content.',
                    imageUrl: '../../assets/img/best-places.webp',
                    altText: '...'
                },
                
            ]
        }
    },
    methods: {
        prevSlide() {
            this.currentSlide = (this.currentSlide - 1 + this.cards.length) % this.cards.length;
        },
        nextSlide() {
            this.currentSlide = (this.currentSlide + 1) % this.cards.length;
        }
    }
}
</script>

<template>
    <!-- creazione template html -->
    <div class="container">
        <div class="row">
            <div class="col">
                <div id="carouselExampleControls" class="carousel" data-bs-ride="carousel">
                    <div class="carousel-inner">
                        <div v-for="(card, index) in cards" :key="index"
                            :class="['carousel-item', { active: index === currentSlide }]">
                            <div class="card">
                                <div class="img-wrapper">
                                    <img :src="card.imageUrl" class="d-block w-100" :alt="card.altText">
                                </div>
                                <div class="card-body">
                                    <h5 class="card-title">{{ card.title }}</h5>
                                    <p class="card-text">{{ card.body }}</p>
                                    <a href="#" class="btn btn-primary">Go somewhere</a>
                                </div>
                            </div>
                        </div>
                    </div>
                    <button class="carousel-control-prev" type="button" @click="prevSlide">
                        <span class="carousel-control-prev-icon" aria-hidden="true"></span>
                        <span class="visually-hidden">Previous</span>
                    </button>
                    <button class="carousel-control-next" type="button" @click="nextSlide">
                        <span class="carousel-control-next-icon" aria-hidden="true"></span>
                        <span class="visually-hidden">Next</span>
                    </button>
                </div>
            </div>
        </div>
    </div>
</template>

<style scoped lang="scss">
/* aggiunta stile css */
@use '../../styles/partials/variables.scss' as*;

.card {
    margin: 0 0.5em;
    box-shadow: 2px 6px 8px 0 rgba(22, 22, 26, 0.18);
    border: none;
}

.carousel-control-prev,
.carousel-control-next {
    background-color: #e1e1e1;
    width: 6vh;
    height: 6vh;
    border-radius: 50%;
    top: 50%;
    transform: translateY(-50%);
}

@media (min-width: 768px) {
    .carousel-item {
        margin-right: 0;
        flex: 0 0 33.333333%;
        display: block;
    }

    .carousel-inner {
        display: flex;
    }
}

.card .img-wrapper {
    max-width: 100%;
    height: 13em;
    display: flex;
    justify-content: center;
    align-items: center;
}

.card img {
    max-height: 100%;
}

@media (max-width: 767px) {
    .card .img-wrapper {
        height: 17em;
    }
}
</style>