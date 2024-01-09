<script>
export default {
    data() {
        return {
            // ARRAY CHE CONTIENE GLI ELEMENTI DEL BANNER AZZURRO
            infoBannerShop: [
                {
                    name: 'DIGITAL COMICS',
                    img: '../img/buy-comics-digital-comics.png',
                },
                {
                    name: 'DC MERCHANDISE',
                    img: '../img/buy-comics-merchandise.png',
                },
                {
                    name: 'SUBSCRIPTION',
                    img: '../img/buy-comics-subscriptions.png',
                },
                {
                    name: 'COMIC SHOP LOCATOR',
                    img: '../img/buy-comics-shop-locator.png',
                },
                {
                    name: 'DC POWER VISA',
                    img: '../img/buy-dc-power-visa.svg',
                },
            ]
        }
    },
    methods: {
        // FUNZIONE PER RECUPERARE IL PATH DELLE IMMAGINI
        getImagePath: function (imgPath) {
            let url = new URL(imgPath, import.meta.url).href;
            return url
        }
    },
}

</script>

<template>
    <!-- INFO BANNER SECTION -->
    <div class="container">

        <div class="row justify-content-between">

            <div class="col-2" v-for="(item, index) in infoBannerShop" :key="index">
                <div class="d-flex h-100 align-items-center justify-content-center">
                    <img :src="getImagePath(item.img)" :alt="item.name">
                    <h5>{{ item.name }}</h5>
                </div>
            </div>

        </div>

    </div>
</template>

<style lang="scss" scoped>
@use '../styles/general.scss' as *;
@use '../styles/partials/variables' as *;

h5 {
    font-size: 15px;
    color: white;
    padding: 0px 15px;
}

img {

    width: 50px;
    height: 60px
}
</style>