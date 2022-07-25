<template>
 <div class="card">
 <h3>
    
    {{product.title}}
    <h5 class="img">Image: {{product.img}}
    </h5>
    <h5 class="url">URL: {{product.url}}
    </h5>
    <h5 class="price">Price: {{product.price}}$
    </h5>
    <h5 class="ratings">RATINGS: {{product.ratings}}
    </h5>
    <p class="description"> Description: {{product.description}}</p>
    <p class="text-muted"> {{product.title}}</p>
    <button class="view-product-button" @click="$emit('view-product',product)">View </button>
 </h3>
    
 </div>

</template>

<script>
    export default {
        props: ['product'],
        computed:{
            description(){
                return this.product.description.substring(0,150)
            }
        }

    }
</script>

<style lang="scss">
.card {
    width: 80%;
    margin: 10%;
    padding: 10px;
    border-radius: 5px;
    background-color: white;
    box-shadow: 0 0 5px gray;
    h5.price {
        color: gray;
    }
    p.description {
        font-size: .85rem;
    }
    p.text-muted {
        color: gray;
    }
}
button.view-product-button {
        padding: 10px;
        background-color: rgb(79, 160, 187);
        border: none;
        color: white;
        font-weight: bold;
        font-size: 1.15rem;
        border-radius: 5px;
        cursor: pointer;
    }
@media (min-width: 500px) {
    .card {
        width: 350px;
        margin: 10px;
    }
}
</style>