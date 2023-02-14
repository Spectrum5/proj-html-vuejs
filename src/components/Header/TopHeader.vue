<script>
export default {
    data() {
        return {

        }
    }
}
</script>

<template>
    <!-- creazione template html -->
    <div class="container-top-header">
        <div class="container">
            <div class="row text-white fw-bold">
                <div class="col-2 text-center d-flex align-items-center">
                    <div class="news-updates text-uppercase p-2 h-100 d-flex align-items-center">
                        news update
                    </div>
                    <div class="news-image">
                        <img src="../../assets/img/best-places-300x200.webp" alt="News image">
                    </div>
                </div>

                <div class="col-8 d-flex align-items-center">
                    <div class="">
                        Center NEWS
                    </div>
                </div>

                <div class="col-2 d-flex justify-content-end align-items-center">
                    <ul class="d-flex align-items-center h-100 list-unstyled mt-auto">
                        <li class="me-3">
                            <a href="#">
                                <font-awesome-icon icon="fa-brands fa-facebook"/>
                            </a>
                        </li>
                        <li class="me-3">
                            <a href="#">
                                <font-awesome-icon icon="fa-brands fa-twitter"/>
                            </a>
                        </li>
                        <li class="me-3">
                            <a href="#">
                                <font-awesome-icon icon="fa-brands fa-instagram"/>
                            </a>
                        </li>
                        <li>
                            <a href="#">
                                <font-awesome-icon icon="fa-brands fa-youtube"/>
                            </a>
                        </li>
                    </ul>
                </div>
            </div>
        </div>

    </div>
</template>

<style scoped lang="scss">
@use '../../styles/partials/variables.scss' as*;

/* aggiunta stile css */
.container-top-header {
    background-color: $background_red;
}

.news-updates {
    background-color: $background_dark;
}

.news-image {
    height: 100%;
    img {
        width: 60px;
        height: 100%;
    }
}
    
ul {
    li{
        a {
            text-decoration: none;
            color: inherit;
            font-size: 1.4rem;
        }
    }
}
</style>