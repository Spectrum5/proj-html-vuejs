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
    <div class="container-fluid p-4 mt-4 mb-2">
        <div class="container">
            <div class="row">
                <div class="col-12">
                    <img class="w-100 rounded" src="../../assets/img/page-banner-1.webp" alt="">
                </div>
            </div>
        </div>
    </div>
</template>

<style scoped lang="scss">
/* aggiunta stile css */
@use '../../styles/partials/variables.scss' as*;

.container-fluid {
    background-color: $background_light;
}
</style>