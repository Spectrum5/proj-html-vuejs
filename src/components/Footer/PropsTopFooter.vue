<script>


export default {
    props: {
        contactStarted: Array,
        contactAbout: Array,
        contactFeatures: Array,
        contactLinks: Array,
    }
}
</script>
<template>
    <div class="container p-3">
        <div class="row">
            <div class="col-2">
                <h5>get started</h5>
                <ul>
                    <li v-for="(item, index) in contactStarted" :key="index">
                        <a href="#nogo">{{ item.label }}</a>
                    </li>
                </ul>
            </div>
            <div class="col-2">
                <h5>about</h5>
                <ul>
                    <li v-for="(item, index) in contactAbout" :key="index">
                        <a href="#nogo">{{ item.label }}</a>
                    </li>
                </ul>
            </div>
            <div class="col-2">
                <h5>features</h5>
                <ul>
                    <li v-for="(item, index) in contactFeatures" :key="index">
                        <a href="#nogo">{{ item.label }}</a>
                    </li>
                </ul>
            </div>
            <div class="col-2">
                <h5>quick links</h5>
                <ul>
                    <li v-for="(item, index) in contactLinks" :key="index">
                        <a href="#nogo">{{ item.label }}</a>
                    </li>
                </ul>
            </div>
            <div class="col-4">
                <div class="newslatter d-flex flex-column text-center">
                    <h5>subscribe to newslatter</h5>
                    <input placeholder="Email" type="email" class="form-control ">
                    <button class="btn btn-dark mt-2 text-uppercase">subscribe</button>
                </div>
            </div>
        </div>
        <hr class="text-white">
</div>
</template>
<style scoped lang="scss" >
@use '../../styles/partials/variables.scss' as*;

ul {
    color: $text_white;
    list-style-type: none;
    padding: 0;
}

h5 {
    color: $text_white;
    text-transform: uppercase;
}

a {
    text-decoration: none;
    color: $text_white;

    &:hover {
        color: $text_dark;
    }
}
</style>