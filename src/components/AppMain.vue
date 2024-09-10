<script>
export default {
}
</script>

<template>
    <main>
        <div class="container">
            <div class="main-content">
                --&gt; Content goes here &lt;--
            </div>
        </div>
    </main>
</template>

<style lang="scss" scoped>
@use '../assets/scss/partials/variables' as *;

main {
    background-image: url('/img/fondo-pag-speciali.jpg');
    background-position: center;
    background-size: cover;

    .main-content {
        text-align: center;
        padding: 50px 0;
        color: $mainBlue;
        font-weight: bold;
        font-size: 1.5rem;
    }
}
</style>