<script>
import InfoBanner from '../components/InfoBanner.vue'
import ComicApp from '../components/ComicApp.vue'
import MainJumbotron from '../components/MainJumbotron.vue'

export default {
    components: {
        InfoBanner,
        ComicApp,
        MainJumbotron
    },
    data() {
        return {
            // ARRAY DEI FUMETTI
            comics: [
                {
                    "thumb": "https://www.coverbrowser.com/image/action-comics/1-1.jpg",
                    "price": "$19.99",
                    "series": "Action Comics",
                    "type": "comic book"
                },
                {
                    "thumb": "https://www.panini.it/media/catalog/product/cache/a5b5dd3adfe0d321084804c738f29601/M/1/M1BLLA015ISBN_0.jpg",
                    "price": "$3.99",
                    "series": "American Vampire 1976",
                    "type": "comic book"
                },
                {
                    "thumb": "https://media.wired.com/photos/593384dad80dd005b42b2817/master/w_2560%2Cc_limit/Aquaman-16.jpg",
                    "price": "$16.99",
                    "series": "Aquaman",
                    "type": "graphic novel"
                },
                {
                    "thumb": "https://d29xot63vimef3.cloudfront.net/image/batgirl/1-1.jpg",
                    "price": "$2.99",
                    "series": "Batgirl",
                    "type": "comic book"
                },
                {
                    "thumb": "https://static.posters.cz/image/750/locandine-film-in-plexiglass-batman-prowl-comic-cover-i69653.jpg",
                    "price": "$3.99",
                    "series": "Batman",
                    "type": "comic book"
                },
                {
                    "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/5/50/Batman_Beyond_v.1_1.jpg",
                    "price": "$2.99",
                    "series": "Batman Beyond",
                    "type": "comic book"
                },
                {
                    "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/0/0d/Batman_Superman_Vol_1_1.jpg",
                    "price": "$3.99",
                    "series": "Batman/Superman",
                    "type": "comic book"
                },
                {
                    "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/c/cf/Batman_Superman_Annual_Vol_2_1.jpg",
                    "price": "$4.99",
                    "series": "Batman/Superman Annual",
                    "type": "comic book"
                },
                {
                    "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/5/54/Batman_The_Joker_War_Zone_Vol_1_1.jpg",
                    "price": "$5.99",
                    "series": "Batman: The Joker War Zone",
                    "type": "comic book"
                },
                {
                    "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/6/64/Batman_Three_Jokers_Collected.jpg",
                    "price": "$6.99",
                    "series": "Batman: Three Jokers",
                    "type": "comic book"
                },
                {
                    "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/f/f8/Batman_White_Knight_Presents_Harley_Quinn_Vol_1_1.jpg",
                    "price": "$4.99",
                    "series": "Batman: White Knight Presents: Harley Quinn",
                    "type": "comic book"
                },
                {
                    "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/c/c8/Catwoman_Vol_2_1.jpg",
                    "price": "$16.99",
                    "series": "Catwoman",
                    "type": "graphic novel"
                }
            ]
        }
    },
    methods: {

    },
}
</script>

<template>
    <main>

        <!-- MAIN CONTENT SECTION -->

        <!-- JUMBOTRON COMPONENT -->
        <MainJumbotron></MainJumbotron>

        <!-- COMICS CARD SECTION-->
        <div class='comics-card-container'>
            <div class="container">

                <div class="row">
                    <!-- COMICS CARD COMPONENT -->
                    <ComicApp class="my-4" v-for="(comic, index) in comics" :key="index" :comic="comic"></ComicApp>

                    <div class="text-center mt-5">
                        <button type="button" class="default-btn"> LOAD MORE </button>
                    </div>
                </div>

            </div>
        </div>

        <!-- INFO BANNER COMPONENTS -->
        <div class="info-banner-container">
            <InfoBanner></InfoBanner>
        </div>

    </main>
</template>
<style lang="scss" scoped>
@use '../styles/general.scss' as *;
@use '../styles/partials/variables' as *;
@use '../styles/partials/mixin' as *;

// MAIN STYLES
main {
    .comics-card-container {
        background-color: $dc_black;
        padding: 70px 0px;
    }

    h3 {
        color: white;
        padding: 100px 0px;
    }

    .info-banner-container {
        background-color: $dc_blue;
        padding: 70px 0px;
    }

    button {
        @include default_btn;
        background-color: $dc_blue;
        border: 1px solid $dc_blue;
        font-size: 14px;
    }



}
</style>