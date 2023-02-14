<script>
export default {
    props: {
        url: String,
        title: String,
        text: String,
        sliderCards: Array,

    }
}
</script>
<template>
    <div v-for="(item, index) in sliderCards" class="card border-0">
        <img class="mb-1 rounded-top" :src="sliderCards[index].img" alt="#">
        <div class="text-center">
            <h5>{{ sliderCards[index].title }}</h5>
            <h6>{{ sliderCards[index].text }}</h6>
        </div>
    </div>
</template>

<style scoped lang="scss">
/* aggiunta stile css */
@use '../../../styles/partials/variables.scss' as*;

.card {
    width: calc(100% / 4 - 15px);
    margin: 20px 5px 20px 10px;
}
</style>