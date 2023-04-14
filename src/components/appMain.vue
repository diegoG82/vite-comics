<script>
import appCard from "./appCard.vue";
export default {
    name: "appMain",
    components: {
        appCard
    },

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
            ],


            superheroimg: [
                {
                    thumb: 'https://www.coverbrowser.com/image/action-comics/1-1.jpg',
                    price: '$19.99',
                    series: 'Action Comics',
                    type: 'comic book',
                },
                {
                    thumb: 'https://www.panini.it/media/catalog/product/cache/a5b5dd3adfe0d321084804c738f29601/M/1/M1BLLA015ISBN_0.jpg',
                    price: '$3.99',
                    series: 'American Vampire 1976',
                    type: 'comic book',
                },
                {
                    thumb: 'https://media.wired.com/photos/593384dad80dd005b42b2817/master/w_2560%2Cc_limit/Aquaman-16.jpg',
                    price: '$16.99',
                    series: 'Aquaman',
                    type: 'graphic novel',
                },
                {
                    thumb: 'https://d29xot63vimef3.cloudfront.net/image/batgirl/1-1.jpg',
                    price: '$2.99',
                    series: 'Batgirl',
                    type: 'comic book',
                },
                {
                    thumb: 'https://static.posters.cz/image/750/locandine-film-in-plexiglass-batman-prowl-comic-cover-i69653.jpg',
                    price: '$3.99',
                    series: 'Batman',
                    type: 'comic book',
                },
                {
                    thumb: 'https://static.wikia.nocookie.net/marvel_dc/images/5/50/Batman_Beyond_v.1_1.jpg',
                    price: '$2.99',
                    series: 'Batman Beyond',
                    type: 'comic book',
                },
                {
                    thumb: 'https://static.wikia.nocookie.net/marvel_dc/images/0/0d/Batman_Superman_Vol_1_1.jpg',
                    price: '$3.99',
                    series: 'Batman/Superman',
                    type: 'comic book',
                },
                {
                    thumb: 'https://static.wikia.nocookie.net/marvel_dc/images/c/cf/Batman_Superman_Annual_Vol_2_1.jpg',
                    price: '$4.99',
                    series: 'Batman/Superman Annual',
                    type: 'comic book',
                },
                {
                    thumb: 'https://static.wikia.nocookie.net/marvel_dc/images/5/54/Batman_The_Joker_War_Zone_Vol_1_1.jpg',
                    price: '$5.99',
                    series: 'Batman: The Joker War Zone',
                    type: 'comic book',
                },
                {
                    thumb: 'https://static.wikia.nocookie.net/marvel_dc/images/6/64/Batman_Three_Jokers_Collected.jpg',
                    price: '$6.99',
                    series: 'Batman: Three Jokers',
                    type: 'comic book',
                },
                {
                    thumb: 'https://static.wikia.nocookie.net/marvel_dc/images/f/f8/Batman_White_Knight_Presents_Harley_Quinn_Vol_1_1.jpg',
                    price: '$4.99',
                    series: 'Batman: White Knight Presents: Harley Quinn',
                    type: 'comic book',
                },
                {
                    thumb: 'https://static.wikia.nocookie.net/marvel_dc/images/c/c8/Catwoman_Vol_2_1.jpg',
                    price: '$16.99',
                    series: 'Catwoman',
                    type: 'graphic novel',
                },
            ]

        }

    },


    methods: {
        getImage(element) {
            return new URL(`../assets/img/${element.images}`, import.meta.url).href;
        }
    }
}

</script>


<template>
    <div class="main">
        <div class="maincontent">
            <div class="contentjumbo">

            </div>

            <div class="topbutton"><button>CURRENT SERIES</button></div>

            <div class="row flex">

                <appCard v-for="(product, index) in superheroimg" :key="index" :thumb="product.thumb"
                    :series="product.series" />

            </div>
            <div class="mainbutton"><button>LOAD MORE</button></div>
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
    // height: 800px;
    width: 100%;
    // margin: 20px auto;
    background-color: black;

    .contentjumbo {
        height: 300px;
        background-image: url(../assets/img/jumbotron.jpg);

        img {
            height: 300px;
            width: 100%;
        }

    }

    .row {
        // height: 800px;
        width: 80%;
        margin: 0 auto;
        margin-top: 20px;
        flex-wrap: wrap;
    }



    .content {
        width: 80%;
        color: white;
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

.mainbutton {
  text-align: center;
  padding: 10px;
  button{
    padding:10px 30px;
    border: none;
    background-color: rgb(2, 130, 249);
    color: white;
  }
}


.topbutton {
   padding: 20px;
   button{
    padding: 10px 30px;
    border: none;
    background-color: rgb(2, 130, 249);
    color: white;
    position: relative;
    bottom: 40px;
    left:180px;
   }
  }
</style>