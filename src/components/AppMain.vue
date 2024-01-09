<script>
import InfoBanner from '../components/InfoBanner.vue'

export default {
    components: {
        InfoBanner,
    },
    data() {
        return {

        }
    },
    methods: {

    },
}
</script>

<template>
    <main>

        <!-- MAIN CONTENT SECTION -->
        <div class='comics-card-container'>
            <div class="container">

                <div class="row">
                    <!-- COMICS CARD SECTION-->
                    <div class="col-12">
                        <h3> Content goes here </h3>
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

// MAIN STYLES
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
        padding: 70px 0px;
    }



}
</style>