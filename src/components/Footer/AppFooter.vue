<script>
import TopFooter from "../../components/Footer/TopFooter.vue"
import BottomFooter from "../../components/Footer/BottomFooter.vue"

export default {
    components: {
        TopFooter,
        BottomFooter,
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
    <BottomFooter />
</template>

<style scoped lang="scss">
/* aggiunta stile css */
@use '../../styles/partials/variables.scss' as*;
footer {
        background-color: $background_red;
    }

</style>