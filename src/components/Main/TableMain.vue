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
                        <font-awesome-icon icon="fa-solid fa-calendar-days" class="me-2"/>{{ store.info[1].text }}
                        <h6>{{ store.info[1].title }}</h6>
                        <p class="categoria" >{{store.info[1].category}}</p>
                        
                    </div>
                </div>
                <div id="background-img-2"
                    class="card background-filter border-0 rounded mt-1 d-flex justify-content-end">
                    <div class="content">
                        <font-awesome-icon icon="fa-solid fa-user" class="me-2" />{{ store.info[7].demo }}
                        <font-awesome-icon icon="fa-solid fa-calendar-days" class="me-2"/>{{ store.info[7].text }}
                        <h6>{{ store.info[7].title }}</h6>
                        <p class="categoria" >{{store.info[2].category}}</p>
                    </div>
                </div>
            </div>
            <div class="col-6">
                <div id="background-img-3"
                    class="card border-0 background-filter rounded p-2 d-flex justify-content-end">
                    <div class="content">
                        <font-awesome-icon icon="fa-solid fa-user" class="me-2" />{{ store.info[0].demo }}
                        <font-awesome-icon icon="fa-solid fa-calendar-days" class="me-2"/>{{ store.info[0].text }}
                        <h6>{{ store.info[0].title }}</h6>
                        <p class="categoria" >{{store.info[3].category}}</p>
                    </div>
                </div>
            </div>
            <div class="col-3">
                <div id="background-img-4" class="card background-filter border-0 rounded d-flex justify-content-end">
                    <div class="content">
                        <font-awesome-icon icon="fa-solid fa-user" class="me-2" />{{ store.info[6].demo }}
                        <font-awesome-icon icon="fa-solid fa-calendar-days" class="me-2" />{{ store.info[6].text }}
                        <h6>{{ store.info[6].title }}</h6>
                        <p class="categoria" >{{store.info[4].category}}</p>
                    </div>
                </div>
                <div id="background-img-5"
                    class="card background-filter border-0 rounded mt-1 d-flex justify-content-end">
                    <div class="content">
                        <font-awesome-icon icon="fa-solid fa-user" class="me-2" />{{ store.info[3].demo }}
                        <font-awesome-icon icon="fa-solid fa-calendar-days" class="me-2"/>{{ store.info[3].text }}
                        <h6>{{ store.info[3].title }}</h6>
                        <p class="categoria" >{{store.info[5].category}}</p>
                    </div>
                </div>

            </div>
        </div>
    </div>
</template>

<style scoped lang="scss">
/* aggiunta stile css */
@use '../../styles/partials/variables.scss' as*;
@use '../../styles/partials/mixins.scss' as*;

.background-filter {
    background-size: contain;
    filter: brightness(80%);
    text-align: center;
    color: $text_white;
}
.categoria{
        color: $text_dark;
        @include categoria;
    }

#background-img-1 {
    background-image: url('../../assets/img/anime-fashion.webp');
    background-repeat: no-repeat;
    width: 100%;
    background-size: cover;
}

#background-img-2 {
    background-image: url('../../assets/img/travel-alone.webp');
    background-repeat: no-repeat;
    width: 100%;
    background-size: cover;
}

#background-img-3 {
    background-image: url('../../assets/img/best-places.webp');
    height: 100%;
    background-repeat: no-repeat;
    background-position: center center;
    background-size: cover;
    width: 100%;
}

#background-img-5 {
    background-image: url('../../assets/img/visit-france.webp');
    background-repeat: no-repeat;
    width: 100%;
    background-size: cover;
}

#background-img-4 {
    background-image: url('../../assets/img/healthy-foods.webp');
    background-repeat: no-repeat;
    width: 100%;
    background-size: cover;
}

.card.background-filter {
    height: 200px;
}
</style>