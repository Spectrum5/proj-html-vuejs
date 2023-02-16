<script>




import PropsTopFooter from './PropsTopFooter.vue'
export default {
    components: {
        PropsTopFooter,
    },
    data() {
        return {
            contactStarted: [
                {
                    label: 'Resuorces'
                },
                {
                    label: 'Tutorials'
                },
                {
                    label: 'Examples'
                },
                {
                    label: 'Docs'
                },
            ],
            contactAbout: [
                {
                    label: 'Stories'
                },
                {
                    label: 'Community'
                },
                {
                    label: 'Blog'
                },
                {
                    label: 'Brand Assets'
                },
            ],
            contactFeatures: [
                {
                    label: 'Overview'
                },
                {
                    label: 'Design'
                },
                {
                    label: 'Code'
                },
                {
                    label: 'Collaborate'
                },
            ],
            contactLinks: [
                {
                    label: 'Stories'
                },
                {
                    label: 'Community'
                },
                {
                    label: 'Blog'
                },
                {
                    label: 'Brand Assets'
                },
            ],

        }
    }
}
</script>
<template>
    <footer>
        <PropsTopFooter :contactStarted="contactStarted" :contactAbout="contactAbout" :contactFeatures="contactFeatures"
            :contactLinks="contactLinks" />
</footer>
</template>
<style scoped lang="scss" >
@use '../../styles/partials/variables.scss' as*;

footer {
    height: 300px;
    background-color: $background_red;
    padding-top: 40px;
    margin-top: 20px;
}
</style>