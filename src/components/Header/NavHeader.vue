<script>

export default {
    data() {
        return {

        }
    }
}
</script>

<template><!-- creazione template html -->
    <div class="container">
        <div class="row">
            <div class="col-2 d-flex align-items-center">
                <font-awesome-icon icon="fa-solid fa-bars" class="fs-3" />
            </div>
            <div class="col-8">
                <ul class="d-flex justify-content-center align-items-center h-100 list-unstyled text-uppercase">
                    <li class="me-4">
                        <a href="#">
                            <font-awesome-icon icon="fa-solid fa-house-chimney" class="me-2" />
                            <span>home</span>
                        </a>
                    </li>
                    <li class="me-4">
                        <a href="#">
                            <font-awesome-icon icon="fa-solid fa-suitcase" class="me-2" />
                            <span>lifestyle</span>
                        </a>
                    </li>
                    <li class="me-4">
                        <a href="#">
                            <font-awesome-icon icon="fa-solid fa-book-open-reader" class="me-2" />
                            <span>stories</span>
                        </a>
                    </li>
                    <li class="me-4">
                        <a href="#">
                            <font-awesome-icon icon="fa-solid fa-book" class="me-2" />
                            <span>pages</span>
                        </a>
                    </li>
                    <li class="me-4">
                        <a href="#">
                            <font-awesome-icon icon="fa-solid fa-user" class="me-2" />
                            <span>about us</span>
                        </a>
                    </li>
                </ul>
            </div>
            <div class="col-2 d-flex align-items-center justify-content-end">
                <div class="search-box">
                    <button class="btnn-search"><font-awesome-icon icon="fa-solid fa-magnifying-glass"
                            class="fs-3" /></button>
                    <input type="text" class="input-search" placeholder="Cerca...">
                </div>
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

.search-box {
    width: fit-content;
    height: fit-content;
    position: relative;
}

.input-search {
    height: 48px;
    width: 40px;
    border-style: none;
    padding: 10px;
    font-size: 16px;
    outline: none;
    border-radius: 25px;
    transition: all .5s ease-in-out;
    background-color: $background_red;
    padding-right: 40px;
    color: $text_white;
}

.input-search::placeholder {
    color: $text_white;
    font-size: 18px;
    font-weight: 100;
}

.btnn-search {
    width: 50px;
    height: 50px;
    border-style: none;
    font-size: 20px;
    font-weight: bold;
    outline: none;
    cursor: pointer;
    border-radius: 50%;
    position: absolute;
    right: 0px;
    color: $text_white;
    background-color: transparent;
    pointer-events: painted;
}

.btnn-search:focus~.input-search {
    width: 200px;
    border-radius: 0px;
    border-bottom: 1px solid rgba(255, 255, 255, .5);
    transition: all 500ms cubic-bezier(0, 0.110, 0.35, 2);
}

.input-search:focus {
    width: 300px;
    border-radius: 0px;
    border-bottom: 1px solid rgba(255, 255, 255, .5);
    transition: all 500ms cubic-bezier(0, 0.110, 0.35, 2);
}</style>