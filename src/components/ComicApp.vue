<script>
export default {
    props: {
        comic: Object,
    }
}
</script>

<template>
    <div class="col-2">
        <!-- COMIC CARD -->
        <div>
            <div class="img-container p-relative">
                <img :src="comic.thumb" :alt="comic.series">
                <span class="price-tag">{{ comic.price }}</span>
            </div>
            <div>
                <h5>{{ comic.series }}</h5>
            </div>
        </div>
    </div>
</template>

<style lang="scss" scoped>
@use '../styles/general.scss' as *;
@use '../styles/partials/variables' as *;

// COMIC STYLE

h5 {
    color: white;
    text-transform: uppercase;
    margin-top: 10px;
    font-size: 15px;
}

.price-tag {
    color: white;
    background-color: $dc_blue;
    padding: 2px 7px;
    font-size: 13px;
    border-radius: 10px;
    position: relative;
    bottom: 220px;
    left: 153px;
}

.img-container {


    img {
        width: 190px;
        height: 230px;
        object-fit: cover;
        object-position: top;

    }

}
</style>