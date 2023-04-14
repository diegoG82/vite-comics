<script>
export default {
    name: "appCard",
    props: {
        thumb: String,
        series: String,

    }
}
</script>

<template>
    <div class="card">
        <img :src="thumb" alt="">
        <h4>{{ series }}</h4>
    </div>
</template>

<style lang="scss" scoped>
.card {
    width: calc(100% / 6 - 20px);
    margin: 10px;


    img {
        max-height: 70%;
        object-fit: contain;
    }

    h4 {
        color: white;
        margin-top: 5px;
    }

}
</style>