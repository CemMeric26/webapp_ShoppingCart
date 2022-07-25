<template>
    <div class="cart-item-card">
        <h3>
        Cart Total: ${{cart_total.toFixed(2)}}
        </h3>
        <button class="view-product-button">credit card pay</button>
    </div>
</template>

<script>
export default {
    
    computed:{
        cart_total(){
            return this.$store.getters.cartTotal
        }
    }
    
}

</script>