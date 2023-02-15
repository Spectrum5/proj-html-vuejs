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

<template >
    <div class="container py-3">
        <div class="row py-2">
            <div class="col d-flex justify-content-between">
                <div>
                    <h3 class="text-uppercase">Lifestyle & stories</h3>
                </div>
                <div>
                    <button class="btn btn-secondary mx-1 text-uppercase">all</button>
                    <button class="btn btn-secondary mx-1 text-uppercase">lifestyle</button>
                    <button class="btn btn-secondary mx-1 text-uppercase">stories</button>
                </div>

            </div>
        </div>
        <div class="row">
            <div class="col-8">
                <div id="background-img-1" class="img-col-8  rounded d-flex align-items-end mt-1">
                    <div class="content">
                        <h6>
                            <font-awesome-icon icon="fa-solid fa-user" class="me-2"/>{{ store.info[7].demo }} {{ store.info[7].text }}
                        </h6>
                        <h5>
                            {{ store.info[7].title }}
                        </h5>
                    </div>
                </div>

            </div>
            <div class="col-4">
                <div class="box d-flex">
                    <div id="background-img-2" class="img-box rounded d-flex align-items-end mt-1"></div>
                    <div class="content">
                        <h6>
                            <font-awesome-icon icon="fa-solid fa-user" class="me-2"/>{{ store.info[7].demo }} {{ store.info[7].text }}
                        </h6>
                        <h5>
                            {{ store.info[7].title }}
                        </h5>
                    </div>
                </div>

                <hr>
                <div class="box d-flex">
                    <div id="background-img-3" class=" img-box rounded d-flex align-items-end mt-1"></div>
                    <div class="content">
                        <h6>
                            <font-awesome-icon icon="fa-solid fa-user" class="me-2"/>{{ store.info[0].demo }} {{ store.info[0].text }}
                        </h6>
                        <h5>
                            {{ store.info[0].title }}
                        </h5>
                    </div>
                </div>
                <hr>
                <div class="box d-flex">
                    <div id="background-img-4" class=" img-box rounded d-flex align-items-end mt-1"></div>
                    <div class="content">
                        <h6>
                            <font-awesome-icon icon="fa-solid fa-user" class="me-2"/>{{ store.info[6].demo }} {{ store.info[6].text }}
                        </h6>
                        <h5>
                            {{ store.info[6].title }}
                        </h5>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>
<style lang="scss" scoped>
/* aggiunta stile css */
@use '../../styles/partials/variables.scss' as*;

.img-col-8 {
    aspect-ratio: 100 / 52;
    background-size: contain;
    filter: brightness(50%);

    .content {
        color: white;
        padding: 10px;
    }
}

.content {
    width: 180px;
    margin-left: 10px;
    display: flex;
    flex-direction: column;
    justify-content: center;

    h6 {
        font-size: 12px;
    }

    h5 {
        font-size: 0.9rem;
        font-weight: bold;
    }
}

.img-box {
    width: 180px;
    aspect-ratio: 100 / 68;
    background-size: contain;
    filter: brightness(50%);

    .content {
        padding: 10px;
        text-align: center;
    }
}

#background-img-1 {
    background-image: url('../../assets/img/success-story.webp');
}

#background-img-2 {
    background-image: url('../../assets/img/travel-alone.webp');

}

#background-img-3 {
    background-image: url('../../assets/img/best-places.webp');
}

#background-img-4 {
    background-image: url('../../assets/img/rice-ball.webp');
}
</style>