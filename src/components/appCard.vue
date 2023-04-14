<script>
export default {
    name: "appCard",
    props: {
        image: String,
        title: String,

    }
}
</script>

<template>
    <div class="card" :class="type">
        <img :src="image" alt="">
        <h4>{{ title }}</h4>
    </div>
</template>

<style lang="scss" scoped>
.card {
    width: calc(100% / 6 - 20px);
    margin: 10px;
    

    img {
        height: 70%;
    }

    h4 {
        color: white;
        margin-top: 5px;
    }

}
</style>