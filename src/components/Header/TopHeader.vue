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
                    <div class="news-updates text-uppercase p-2">
                        news update
                    </div>
                    <div>
                        image
                    </div>
                </div>

                <div class="col-8 d-flex align-items-center">
                    Center NEWS
                </div>

                <div class="col-2 d-flex justify-content-end align-items-center">
                    SOCIAL
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
</style>