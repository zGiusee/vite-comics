<script>

</script>

<template>
    <div class="jumbo-container">
        <span class="default-badge-bg">CURRENT SERIES</span>

    </div>
</template>

<style lang="scss" scoped>
@use '../styles/general.scss' as *;
@use '../styles/partials/variables' as *;
@use '../styles/partials/mixin' as *;

.default-badge-bg {
    @include default_badge_bg;
    background-color: $dc_blue;
    position: absolute;
    bottom: -25px;
    left: 300px;
}

.jumbo-container {
    position: relative;
    height: 450px;
    background-size: cover;
    background-image: url(../img/jumbotron.jpg);


}
</style>