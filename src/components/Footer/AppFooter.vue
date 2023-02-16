<script>
import TopFooter from "../../components/Footer/TopFooter.vue"

export default {
    components: {
        TopFooter,
    },
    data() {
        return {

        }
    }
}
</script>

<template>
    <!-- creazione template html -->
    <TopFooter />
</template>

<style scoped lang="scss">
/* aggiunta stile css */
@use '../../styles/partials/variables.scss' as*;
footer {
    background-color: $background_red;
}
</style>