<script>
export default {
    data() {
        return {
            footerColumnTwoLinks: [
                {
                    label: "Il Pastificio",
                    url: "#",
                    active: false,
                },
                {
                    label: "Grano",
                    url: "#",
                    active: false,
                },
                {
                    label: "Filiera",
                    url: "#",
                    active: false,
                },
                {
                    label: "100 anni di pasta",
                    url: "#",
                    active: false,
                },
                {
                    label: "Sartoria della pasta",
                    url: "#",
                    active: false,
                },
            ],
            footerColumnThreeLinks: [
                {
                    label: "Le Classiche",
                    url: "#",
                    active: false,
                },
                {
                    label: "Le Integrali",
                    url: "#",
                    active: false,
                },
                {
                    label: "Le Speciali",
                    url: "#",
                    active: false,
                },
                {
                    label: "Le Biologiche",
                    url: "#",
                    active: false,
                },
                {
                    label: "Le Gluten-Free",
                    url: "#",
                    active: false,
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
                    <ul>
                        <li
                            v-for="(link, index) in footerColumnTwoLinks"
                            :key="index"
                        >
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
                </div>
                <div class="col-1-3">
                    <h4>Prodotti</h4>
                    <ul>
                        <li
                            v-for="(link, index) in footerColumnThreeLinks"
                            :key="index"
                        >
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
                </div>
            </div>
        </div>
    </footer>
</template>

<style lang="scss" scoped>
@use "../assets/scss/partials/variables" as *;
@use "../assets/scss/partials/mixins" as *;

footer {
  padding: 40px 0 200px 0;
  background-image: url('/img/footer-montagne-bottom.jpg');
  background-position: bottom center;
  background-size: contain;
  background-repeat: no-repeat;

  h4 {
    text-transform: uppercase;
    color: $mainBlue;
    font-size: 1.2rem;
    margin-bottom: 20px;
  }

  ul {
    @include base-ul-rules;

    li {
      a {
        @include base-a-rules;
      }
    }
  }
}
</style>
