<script>
export default {
    data() {
        return {
            text: 'che bello vite!',
        }
    }
}
</script>

<template>
    <!-- creazione template html -->
    <div class="container">
        <p>{{ text }}</p>
    </div>

</template>

<style scoped>
/* aggiunta stile css */
.container {
    background-color: rgb(122, 121, 121, 0.3);
    height: 200px;
    width: 100%;
    align-items: center;
    justify-content: center;
    display: flex;
}

p {
    font-size: 3rem;
}
</style>