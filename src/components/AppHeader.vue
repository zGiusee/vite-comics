<script>
export default {
  data() {
    return {
      links: [
        {
          name: 'CHARACTERS',
          url: '#',
          active: false,
        },
        {
          name: 'COMICS',
          url: '#',
          active: false,
        },
        {
          name: 'MOVIES',
          url: '#',
          active: true,
        },
        {
          name: 'TV',
          url: '#',
          active: false,
        },
        {
          name: 'GAMES',
          url: '#',
          active: false,
        },
        {
          name: 'COLLECTIBLES',
          url: '#',
          active: false,
        },
        {
          name: 'VIDEOS',
          url: '#',
          active: false,
        },
        {
          name: 'FANS',
          url: '#',
          active: false,
        },
        {
          name: 'NEWS',
          url: '#',
          active: false,
        },
        {
          name: 'SHOP',
          url: '#',
          active: false,
        },
      ],
    }
  },

}
</script>

<template>
  <header>
    <div class="container">
      <div class="row py-3">

        <!-- HEADER LEFT SIDE (LOGO) -->
        <div class="col-4">
          <div class=" d-flex align-items-center h-100">
            <img class="logo" src="../img/dc-logo.png" alt="">
          </div>
        </div>


        <!-- HEADER RIGHT SIDE (LIST) -->
        <div class="col-8">
          <div class="header-list-container">

            <ul>
              <li v-for="link, index in links" :key="index"><a :href="link.url" :class="link.active ? 'active' : ''">{{
                link.name }}</a></li>
            </ul>

          </div>
        </div>

      </div>
    </div>

  </header>
</template>

<style lang="scss" scoped>
@use '../styles/general.scss' as *;
@use '../styles/partials/variables' as *;

// HEADER STYLES
header {

  .logo {
    width: 65px;
    vertical-align: middle;
  }

  .header-list-container {
    vertical-align: middle;

    // RIGHT SIDE HEADER LIST
    ul {
      list-style-type: none;
      display: flex;
      margin-bottom: 0px;

      li {
        padding: 18px;
        border: 3px solid transparent;

        &.active,
        &:hover {
          border-bottom: 3px solid $dc_blue;

        }

      }

      a {
        color: $dc_black;
        text-decoration: none;

        &.active,
        &:hover {
          color: $dc_blue;

        }

      }
    }
  }
}
</style>