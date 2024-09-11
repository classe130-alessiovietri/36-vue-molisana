<script>
export default {}
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
    padding: 40px 0;
    text-align: center;
    font-size: 2rem;
    color: $mainBlue;
  }

}
</style>