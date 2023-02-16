<script>

export default {
    data() {
        return {
            menuItems: [
                {
                    label: "home",
                    link: "#nogo",
                    icon: ["fa-solid", "fa-house-chimney"],
                },
                {
                    label: "lifestyle",
                    link: "#nogo",
                    icon: ["fa-solid", "fa-suitcase"],
                },
                {
                    label: "stories",
                    link: "#nogo",
                    icon: ["fa-solid", "fa-book-open-reader"],
                },
                {
                    label: "pages",
                    link: "#nogo",
                    icon: ["fa-solid", "fa-book"],
                },
                {
                    label: "about us",
                    link: "#nogo",
                    icon: ["fa-solid", "fa-user"],
                },
            ],
        };
    },
};
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
                    <li v-for="(item, index) in menuItems" :key="index" class="me-4">
                        <a :href="item.link">
                            <font-awesome-icon :icon="item.icon" class="me-2" />
                            <span>{{ item.label }}</span>
                        </a>
                    </li>
                </ul>
            </div>
            <div class="col-2 d-flex align-items-center justify-content-end">
                <div class="search-box">
                    <button class="btnn-search">
                        <font-awesome-icon icon="fa-solid fa-magnifying-glass" class="fs-3" />
                    </button>
                    <input type="text" class="input-search" placeholder="Cerca..." />
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
    height: 50px;
    width: 50px;
    border-style: none;
    padding: 10px;
    font-size: 1.3rem;
    outline: none;
    border-radius: 25px;
    transition: all .5s ease-in-out;
    background-color: $background_red;
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
    font-weight: bold;
    outline: none;
    cursor: pointer;
    border-radius: 50%;
    position: absolute;
    right: 0px;
    color: $text_white;
    background-color: transparent;
    pointer-events: painted;

    &:hover {
        background-color: $background_dark;
    }
}

.btnn-search:focus~.input-search {
    width: 200px;
    border-radius: 0px;
    border-bottom: 1px solid rgba(255, 255, 255, .5);
    transition: all 500ms cubic-bezier(0, 0.110, 0.35, 2);

    &:hover {
        background-color: $background_dark;
    }
}

.input-search:focus {
    width: 300px;
    border-radius: 0px;
    border-bottom: 1px solid rgba(255, 255, 255, .5);
    transition: all 500ms cubic-bezier(0, 0.110, 0.35, 2);

    &:hover {
        background-color: $background_dark;
    }
}
</style>