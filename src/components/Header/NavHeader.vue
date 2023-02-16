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
    <div class="container">
        <div class="row">
            <div class="col-2 d-flex align-items-center">
                <font-awesome-icon icon="fa-solid fa-bars" class="fs-3" />
            </div>
            <div class="col-8">
                <ul class="d-flex justify-content-center align-items-center h-100 list-unstyled text-uppercase">
                    <li class="me-4">
                        <a href="#">
                            <font-awesome-icon icon="fa-solid fa-house-chimney" class="me-2"/>
                            <span>home</span>
                        </a>
                    </li>
                    <li class="me-4">
                        <a href="#">
                            <font-awesome-icon icon="fa-solid fa-suitcase" class="me-2"/>
                            <span>lifestyle</span>
                        </a>
                    </li>
                    <li class="me-4">
                        <a href="#">
                            <font-awesome-icon icon="fa-solid fa-book-open-reader" class="me-2"/>
                            <span>stories</span>
                        </a>
                    </li>
                    <li class="me-4">
                        <a href="#">
                            <font-awesome-icon icon="fa-solid fa-book" class="me-2"/>
                            <span>pages</span>
                        </a>
                    </li>
                    <li class="me-4">
                        <a href="#">
                            <font-awesome-icon icon="fa-solid fa-user" class="me-2"/>
                            <span>about us</span>
                        </a>
                    </li>
                </ul>
            </div>
            <div class="col-2 d-flex align-items-center justify-content-end">
                <font-awesome-icon icon="fa-solid fa-magnifying-glass" class="fs-3" />
            </div>
        </div>

    </div>
</template>

<style scoped lang="scss">
@use '../../styles/partials/variables.scss' as*;

    /* aggiunta stile css */
ul {
    li {
        a {
            text-decoration: none;
            color: inherit;
            font-weight: bold;
        }
    }
}

</style>