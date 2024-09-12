<script>
export default {
    props: {
        productTitle: String,
        productImg: String
    }
};
</script>

<template>
    <div class="product-item">
        <div>
            <img :src="productImg" :alt="productTitle">
        </div>
        <h3>
            {{ productTitle }}
        </h3>
    </div>
</template>

<style lang="scss" scoped>
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