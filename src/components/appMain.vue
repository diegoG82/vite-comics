<script>
export default {
    name: "appMain",

    data() {
        return {
            ctaitems: [
                {
                    name: 'DIGITAL COMICS',
                    images: 'buy-comics-digital-comics.png',
                    url: '#'
                },
                {
                    name: 'DC MERCHANDISE',
                    images: 'buy-comics-merchandise.png',
                    url: '#'
                },
                {
                    name: 'SUBSCRIPTION',
                    images: 'buy-comics-subscriptions.png',
                    url: '#'
                },
                {
                    name: 'COMIC SHOP LOCATOR',
                    images: 'buy-comics-shop-locator.png',
                    url: '#'
                },
                {
                    name: 'DC POWER VISA',
                    images: 'buy-dc-power-visa.svg',
                    url: '#'
                },
            ]
        }

    },

    methods: {
        getImage(element) {
            return new URL(`../img/${element.images}`, import.meta.url).href;
        }
    }
}

</script>


<template>
    <div class="main">
        <div class="maincontent">
            <div class="content flex">CONTENT HERE</div>
        </div>
        <div class="calltoaction flex">
            <div class="content flex">
                <ul class="ctalist flex">

                    <li class="flex" v-for="image in ctaitems">
                        <a class="flex" :href="image.url">
                            <img :src="getImage(image)" alt="">
                            <p>{{ image.name }}</p>
                        </a>
                    </li>

                </ul>
            </div>
        </div>
    </div>
</template>

<style scoped lang="scss">


.maincontent {
    height: 100px;
    width: 100%;
    margin: 0 auto;
    background-color: black;

    .content {
        height: 100px;
        width: 80%;
        color: white;
        line-height: 100px;
        margin: 0 auto;
    }

}

.calltoaction {

    background-color: rgb(2, 130, 249);
    position: relative;
    z-index: 999;

    .content {
        height: 100px;
        width: 70%;
        color: white;
        margin: 0 auto;
    }

    .ctalist {
        width: 100%;
        justify-content: space-between;

    }

    li {
        list-style: none;
        font-size: 1rem;
        justify-content: center;
        align-items: center;

        img {
            height: 50px;
        }
    }

    ul {
        align-items: center;
    }

    p {
        padding-left: 10px;
    }

    a {
        color: inherit;
        align-items: center;
        justify-content: center;
        text-decoration: none;
    }

}
</style>