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
      footerColumnTwoLinks: [
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
      footerColumnThreeLinks: [
        {
          label: 'Le Classiche',
          url: '#',
          active: false
        },
        {
          label: 'Le Integrali',
          url: '#',
          active: false
        },
        {
          label: 'Le Speciali',
          url: '#',
          active: false
        },
        {
          label: 'Le Biologiche',
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
  components: {
  },
  methods: {
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

  <main>
    <div class="container">
      <div class="main-content">
        --&gt; Content goes here &lt;--
      </div>
    </div>
  </main>

  <footer>
    <div class="container">
      <div class="row">
        <div class="col-1-3">
          <img src="/img/la-molisana-logo.png" alt="La Molisana">
        </div>
        <div class="col-1-3">
          <h4>
            Pastificio
          </h4>
          <ul>
            <li v-for="(link, index) in footerColumnTwoLinks" :key="index">
              <a :href="link.url" :class="{
                  'active': link.active
                }">
                {{ link.label }}
              </a>
            </li>
          </ul>
        </div>
        <div class="col-1-3">
          <h4>
            Prodotti
          </h4>
          <ul>
            <li v-for="(link, index) in footerColumnThreeLinks" :key="index">
              <a :href="link.url" :class="{
                  'active': link.active
                }">
                {{ link.label }}
              </a>
            </li>
          </ul>
        </div>
      </div>
    </div>
  </footer>
</template>

<style scoped>
header {
  text-align: center;
  padding: 20px 0;
}

header ul {
  list-style: none;
  display: flex;
  justify-content: center;
  align-items: center;
  padding: 0;
}

header ul li a {
  text-decoration: none;
  color: black;
  display: inline-block;
  padding: 10px;
  font-weight: bold;
  transition: all .2s ease-in-out;
}

header ul li a:hover,
header ul li a.active {
  background-color: #DAE9FE;
}

main {
  background-image: url('/img/fondo-pag-speciali.jpg');
  background-position: center;
  background-size: cover;
}

main .main-content {
  text-align: center;
  padding: 50px 0;
  color: #114674;
  font-weight: bold;
  font-size: 1.5rem;
}

footer {
  padding: 40px 0 200px 0;
  background-image: url('/img/footer-montagne-bottom.jpg');
  background-position: bottom center;
  background-size: contain;
  background-repeat: no-repeat;
}

footer h4 {
  text-transform: uppercase;
  color: #114674;
  font-size: 1.2rem;
  margin-bottom: 20px;
}

footer ul {
  list-style: none;
  padding: 0;
}

footer ul li a {
  text-decoration: none;
  color: black;
  display: inline-block;
}
</style>
