<script>
export default {
    name: "appHeader",

    data() {
        return {
            links: [
                {
                    text: "CHARACTERS",
                    url: "#",
                    current: false
                },

                {
                    text: "COMICS",
                    url: "#",
                    current: true
                },

                {
                    text: "MOVIES",
                    url: "#",
                    current: false
                },

                {
                    text: "TV",
                    url: "#",
                    current: false
                },

                {
                    text: "GAMES",
                    url: "#",
                    current: false
                },

                {
                    text: "COLLECTIBLES",
                    url: "#",
                    current: false
                },

                {
                    text: "VIDEOS",
                    url: "#",
                    current: false
                },

                {
                    text: "FANS",
                    url: "#",
                    current: false
                },

                {
                    text: "NEWS",
                    url: "#",
                    current: false
                },

                {
                    text: "SHOP",
                    url: "#",
                    current: false
                },

            ]
        }
    }
}
</script>
<template>
    <div class="header-container">
        <div class="header flex">
            <div class="header-logo flex"><img class="dclogo" src="../img/dc-logo.png" alt="dclogo"></div>
            <div class="header-list">
                <ul class="header-nav flex">
                    <li v-for="link in links" :class="link.current ? 'active' : ''">
                        <a :href="link.url">{{ link.text }}</a>
                    </li>
                </ul>
            </div>

        </div>


    </div>
</template>



<style scoped lang="scss">
.header-container {
    background-color: white;
}

.header {
    background-color: inherit;
    height: 100px;
    width: 80%;
    margin: 0 auto;

    &-logo {
        width: 40%;
        align-items: center;
        line-height: 100px;
    }

    &-list {
        width: 60%;
        align-items: center;
        line-height: 100px;
    }

    ul {
        justify-content: end;
        gap: 10px
    }

}

li {
    list-style: none;

    &.active,
    &:hover {
        border-bottom: 5px solid rgb(2, 130, 249);
        color: rgb(2, 130, 249);
        height: 95px;
    }
}

a {
    text-decoration: none;
    color: inherit;
    font-weight: bolder;
}

img {
    width: 70px;
}
</style>