<script>
export default {
    data() {
        return {
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
}
</script>

<template>
    <main>

        <div class='comics-card-container'>
            <div class="container">
                <!-- MAIN CONTENT SECTION -->
                <div class="row">
                    <!-- COMICS CARD -->
                    <div class="col-12">
                        <h3> Content goes here </h3>
                    </div>
                </div>

            </div>
        </div>

        <div class="info-banner-container py-4">
            <div class="container">
                <!-- INFO BANNER SECTION -->
                <div class="row justify-content-between">
                    <div class="col-2 " v-for="(item, index) in infoBannerShop" :key="index">
                        <div>
                            <img :src="item.img" alt="">
                            <h5>{{ item.name }}</h5>
                        </div>
                    </div>
                </div>

            </div>
        </div>
    </main>
</template>
<style lang="scss" scoped>
@use '../styles/general.scss' as *;
@use '../styles/partials/variables' as *;

main {
    .comics-card-container {
        background-color: $dc_black;
    }

    h3 {
        color: white;
        padding: 100px 0px;
    }

    .info-banner-container {
        background-color: $dc_blue;

        h5 {
            font-size: 17px;
            color: white;
        }

        img {
            width: 100%;

        }

        ;
    }
}
</style>