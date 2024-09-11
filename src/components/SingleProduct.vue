<script>
export default {
    props: {
        product: Object
    }
};
</script>

<template>
    <div class="product-item">
        <div>
            <img :src="product.src" :alt="product.titolo">
        </div>
        <h3>
            {{ product.titolo }}
        </h3>
    </div>
</template>

<style lang="scss" scoped>
@use "../assets/scss/partials/variables" as *;

.product-item {
    border: 1px solid $mainBlue;
    width: 25%;

    h3 {
        color: $mainBlue;
        text-align: center;
        padding: 4px;
    }

    &.w-50 {
        width: 50%;
    }
}
</style>