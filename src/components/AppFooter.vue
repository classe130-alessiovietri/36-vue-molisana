<script>
export default {
  data() {
    return {
      footerNavOne: [
        {
          label: 'Il Pastificio',
          url: '#',
          active: false
        },
        {
          label: 'Grano',
          url: '#',
          active: false
        },
        {
          label: 'Filiera',
          url: '#',
          active: false
        },
        {
          label: '100 anni di pasta',
          url: '#',
          active: false
        },
        {
          label: 'Sartoria della pasta',
          url: '#',
          active: false
        },
      ],
      footerNavTwo: [
        {
          label: 'Le classiche',
          url: '#',
          active: false
        },
        {
          label: 'Le integrali',
          url: '#',
          active: false
        },
        {
          label: 'Le speciali',
          url: '#',
          active: false
        },
        {
          label: 'Le biologiche',
          url: '#',
          active: false
        },
        {
          label: 'Le Gluten-Free',
          url: '#',
          active: false
        },
      ],
    };
  },
};
</script>

<template>
    <footer>
        <div class="container">
            <div class="row">
                <div class="col-1-3">
                    <img src="/img/la-molisana-logo.png" alt="La Molisana" />
                </div>
                <div class="col-1-3">
                    <h4>Pastificio</h4>

                    <nav>
                        <ul>
                            <li v-for="(link, i) in footerNavOne" :key="i">
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
                <div class="col-1-3">
                    <h4>Prodotti</h4>

                    <nav>
                        <ul>
                            <li v-for="(link, i) in footerNavTwo" :key="i">
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
            </div>
        </div>
    </footer>
</template>

<style lang="scss" scoped>
footer {
  padding: 40px 0 180px 0;
  background-image: url('/img/footer-montagne-bottom.jpg');
  background-size: 100% auto;
  background-position: bottom center;
  background-repeat: no-repeat;

  h4 {
    text-transform: uppercase;
    font-size: 1.5rem;
    margin-bottom: 15px;
    color: $mainBlue;
  }

  ul {
    @include simple-ul;

    li {

      a {
        display: inline-block;
        color: black;
        text-decoration: none;
      }

    }

  }

}
</style>
