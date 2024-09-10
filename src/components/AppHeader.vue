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
            ],
        };
    }
}
</script>

<template>
    <header>
        <div class="container">
            <div>
                <img src="/img/la-molisana-logo.png" alt="La Molisana">
            </div>

            <nav>
                <ul>
                    <li v-for="(link, index) in mainMenuLinks" :key="index">
                        <a :href="link.url" :class="{
                            'active': link.active
                        }">
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
    @include base-ul-rules;
    display: flex;
    justify-content: center;
    align-items: center;

    li {
      a {
        @include base-a-rules;
        padding: 10px;
        font-weight: bold;
        transition: all .2s ease-in-out;

        &:hover, &.active {
          background-color: #DAE9FE;
        }
      }
    }
  }
}
</style>