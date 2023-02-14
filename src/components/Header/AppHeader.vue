<script>
import TopHeader from "../../components/Header/TopHeader.vue"
import LogoHeader from "../../components/Header/LogoHeader.vue"
import NavHeader from "../../components/Header/NavHeader.vue"

export default {
    data() {
        return {
            TopHeader,
            LogoHeader,
            NavHeader,
        }
    }
}
</script>

<template>
    <!-- creazione template html -->
    <TopHeader />
    <LogoHeader />
    <NavHeader />

</template>

<style scoped lang="scss">
    /* aggiunta stile css */
</style>