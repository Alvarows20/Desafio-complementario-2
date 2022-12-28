<template>
    <div>
        <h1>{{tittle}}</h1>
        <h2>{{subtittle}}</h2>
    </div>
</template>

<script>
export default {
    name: 'AppHeader',
    props: {
        tittle: {
            type: String,
            required: true,
        },
        subtittle: {
            type: String,
            required: true,
        },
    },
}
</script>

<style scoped>

    h1 {
        font-size: 22px;
    }
    h2 {
        font-size: 20px;
    }
    
</style>