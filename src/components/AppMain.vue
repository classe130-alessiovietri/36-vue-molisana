<script>
import SingleProduct from './SingleProduct.vue';

export default {
    data() {
        return {
            pastas: [
                {
                    src: "https://www.lamolisana.it/wp-content/uploads/2021/04/1-spaghetto-quadrato.jpg",
                    titolo: "N.4 Spaghetto Quadrato Bucato",
                    tipo: "lunga",
                    cottura: 6,
                },
                {
                    src: "https://www.lamolisana.it/wp-content/uploads/2021/04/5-fettuccine.jpg",
                    titolo: "N.5 Fettuccine",
                    tipo: "lunga",
                    cottura: 13,
                },
                {
                    src: "https://www.lamolisana.it/wp-content/uploads/2021/04/6-linguine.jpg",
                    titolo: "N.6 Linguine",
                    tipo: "lunga",
                    cottura: 12,
                },
                {
                    src: "https://www.lamolisana.it/wp-content/uploads/2021/04/7-mezze-linguine.jpg",
                    titolo: "N.7 Mezze Linguine",
                    tipo: "lunga",
                    cottura: 11,
                },
                {
                    src: "https://www.lamolisana.it/wp-content/uploads/2021/04/11-spaghettino-quadrato.jpg",
                    titolo: "n.11 Spaghettino Quadrato",
                    tipo: "lunga",
                    cottura: 9,
                },
                {
                    src: "https://www.lamolisana.it/wp-content/uploads/2021/05/38-mezze-maniche.jpg",
                    titolo: "N.38 Mezze maniche",
                    tipo: "corta",
                    cottura: 12,
                },
                {
                    src: "https://www.lamolisana.it/wp-content/uploads/2021/05/44-sedani.jpg",
                    titolo: "N.44 Sedani",
                    tipo: "corta",
                    cottura: 8,
                },
                {
                    src: "https://www.lamolisana.it/wp-content/uploads/2021/05/49-sedani.jpg",
                    titolo: "N.49 Sedanini",
                    tipo: "corta",
                    cottura: 8,
                },
                {
                    src: "https://www.lamolisana.it/wp-content/uploads/2021/05/53-lumachine.jpg",
                    titolo: "N.53 Lumachine",
                    tipo: "corta",
                    cottura: 12,
                },
                {
                    src: "https://www.lamolisana.it/wp-content/uploads/2021/05/55-chifferi-rigati.jpg",
                    titolo: "N.55 Chifferi rigati",
                    tipo: "corta",
                    cottura: 12,
                },
                {
                    src: "https://www.lamolisana.it/wp-content/uploads/2021/05/58-misto-corto.jpg",
                    titolo: "N.58 Misto corto",
                    tipo: "corta",
                    cottura: 9,
                },
                {
                    src: "https://www.lamolisana.it/wp-content/uploads/2021/06/84-ditale-quadrato.jpg",
                    titolo: "N.84 Ditale Quadrato",
                    tipo: "cortissima",
                    cottura: 12,
                },
            ]
        };
    },
    components: {
        SingleProduct
    }
};
</script>

<template>
    <main>
        <div class="container">
            <section>
                <h1>
                    Lista Prodotti
                </h1>

                <div class="pastas-container">
                    <SingleProduct
                        v-for="(pasta, i) in pastas"
                        :key="i"
                        :product="pasta" />
                </div>
            </section>

            <section>
                <h2>
                    Prodotti in evidenza
                </h2>

                <div class="pastas-container">
                    <SingleProduct :product="pastas[2]" class="w-50" />
                    <SingleProduct :product="pastas[4]" class="w-50" />
                </div>
            </section>
        </div>
    </main>
</template>

<style lang="scss" scoped>
@use "../assets/scss/partials/variables" as *;

main {
    background-image: url("/img/fondo-pag-speciali.jpg");
    background-position: center;
    background-size: cover;
    padding: 40px 0;

    h1, h2 {
        text-align: center;
        font-size: 1.7rem;
        color: $mainBlue;
        margin: 20px 0;
    }

    .pastas-container {
        background-color: white;
        display: flex;
        flex-wrap: wrap;
    }
}
</style>
