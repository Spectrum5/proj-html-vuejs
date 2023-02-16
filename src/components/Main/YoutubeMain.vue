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
        <div class="row my-5">
            <div class="col d-flex justify-content-center">
                <iframe id="ytplayer" type="text/html" height="600"
                    src="https://www.youtube.com/embed/?listType=playlist&list=PLzSjbEiFKZ_w9zWXjVSTLi5FUlcPHwQCc&autoplay=1"
                    frameborder="0" allowfullscreen>
                </iframe>
            </div>
        </div>
    </div>
</template>

<style scoped lang="scss">
/* aggiunta stile css */
@use '../../styles/partials/variables.scss' as*;

#ytplayer {
    width: 100%;
}
</style>