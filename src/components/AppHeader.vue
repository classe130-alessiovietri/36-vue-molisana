<script>
export default {
    data() {
        return {
            mainMenuLinks: [
                {
                    label: 'Home',
                    url: '#',
                    active: false
                },
                {
                    label: 'Prodotti',
                    url: '#',
                    active: true
                },
                {
                    label: 'Chi Siamo',
                    url: '#',
                    active: false
                },
                {
                    label: 'Contatti',
                    url: '#',
                    active: false
                },
            ]
        };
    }
};
</script>

<template>
    <header>
        <div class="container">
            <div>
                <img src="/img/la-molisana-logo.png" alt="La Molisana" />
            </div>

            <nav>
                <ul>
                    <li v-for="(link, i) in mainMenuLinks" :key="i">
                        <!-- <a :href="link.url" :class="link.active ? 'active' : ''"> -->
                        <a
                            :href="link.url"
                            :class="{
                                active: link.active,
                            }"
                        >
                            {{ link.label }}
                        </a>
                    </li>
                </ul>
            </nav>
        </div>
    </header>
</template>

<style lang="scss" scoped>
@use '../assets/scss/partials/mixins' as *;

header {
  text-align: center;
  padding: 20px 0;

  ul {
    @include simple-ul;
    @include flex-center;

    li {

      a {
        display: inline-block;
        margin: 0 5px;
        padding: 10px;
        color: black;
        text-decoration: none;
        font-weight: bold;
        transition: all .2s ease-in-out;

        // header ul li a:hover, header ul li a.active {
        &:hover, &.active {
          background-color: #DAE9FE;
        }
      }

    }

  }

}
</style>
