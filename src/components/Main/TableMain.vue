<script>
import { store } from '../../store.js'
export default {
    data() {
        return {
            store,
        }
    }
}
</script>

<template>
    <!-- creazione template html -->
    <div class="container pt-5 pb-5">
        <div class="row">
            <div class="col-3 h-100">
                <div id="background-img-1" class="card background-filter border-0 rounded d-flex justify-content-end">
                    <div class="content">
                        <font-awesome-icon icon="fa-solid fa-user" class="me-2" />{{ store.info[1].demo }}
                        {{ store.info[1].text }}
                        <h5>{{ store.info[1].title }}</h5>
                    </div>
                </div>
                <div id="background-img-2"
                    class="card background-filter border-0 rounded mt-1 d-flex justify-content-end">
                    <div class="content">
                        <font-awesome-icon icon="fa-solid fa-user" class="me-2" />{{ store.info[7].demo }}
                        {{ store.info[7].text }}
                        <h5>{{ store.info[7].title }}</h5>
                    </div>
                </div>
            </div>
            <div class="col-6">
                <div id="background-img-3"
                    class="card border-0 background-filter rounded p-2 d-flex justify-content-end">
                    <div class="content">
                        <font-awesome-icon icon="fa-solid fa-user" class="me-2" />{{ store.info[0].demo }}
                        {{ store.info[0].text }}
                        <h5>{{ store.info[0].title }}</h5>
                    </div>
                </div>
            </div>
            <div class="col-3">
                <div id="background-img-4" class="card background-filter border-0 rounded d-flex justify-content-end">
                    <div class="content">
                        <font-awesome-icon icon="fa-solid fa-user" class="me-2" />{{ store.info[6].demo }}
                        {{ store.info[6].text }}
                        <h5>{{ store.info[6].title }}</h5>
                    </div>
                </div>
                <div id="background-img-5"
                    class="card background-filter border-0 rounded mt-1 d-flex justify-content-end">
                    <div class="content">
                        <font-awesome-icon icon="fa-solid fa-user" class="me-2" />{{ store.info[3].demo }}
                        {{ store.info[3].text }}
                        <h5>{{ store.info[3].title }}</h5>
                    </div>
                </div>

            </div>
        </div>
    </div>
</template>

<style scoped lang="scss">
/* aggiunta stile css */
@use '../../styles/partials/variables.scss' as*;

.background-filter {
    background-size: contain;
    filter: brightness(70%);
    text-align: center;
    color: white;
}

#background-img-1 {
    background-image: url('../../assets/img/anime-fashion.webp');
}

#background-img-2 {
    background-image: url('../../assets/img/travel-alone.webp');
}

#background-img-3 {
    background-image: url('../../assets/img/best-places.webp');
    height: 100%;
    background-repeat: no-repeat;
    background-position: center center;
    background-size: cover;
}

#background-img-5 {
    background-image: url('../../assets/img/visit-france.webp');
}

#background-img-4 {
    background-image: url('../../assets/img/healthy-foods.webp');
}

.card.background-filter {
    height: 200px;
}
</style>