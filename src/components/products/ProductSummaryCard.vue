<template>
 <div class="card">
 <h3>
    <h4>{{product.title}}</h4>
    
    <img class="img" :src="product.img">
    
    <h5 class="url">
    <a :href="product.url">Product Link</a>
    </h5>
    
    
    <h5 class="price">Price: {{product.price}}$
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
            },
            
    }
    }
</script>

<style lang="scss">
.card {
    width: 80%;
    margin: 10%;
    padding: 10px;
    border-radius: 50px;
    background-color: rgb(213, 232, 229);
    box-shadow: 0 0 3px rgb(162, 151, 151);
    h5.price {
        color: rgb(207, 33, 33);
    }
    p.description {
        font-size: .85rem;
    }
    p.text-muted {
        color: rgb(131, 0, 124);
    }
}
button.view-product-button {
        padding: 10px;
        background-color: rgb(77, 165, 197);
        border: none;
        color: rgb(227, 46, 18);
        font-weight: bold;
        font-size: 1.15rem;
        border-radius: 50px;
        cursor: pointer;
    }
@media (min-width: 500px) {
    .card {
        width: 350px;
        margin: 10px;
    }
}

.img{
    width: 200px;
    height:200px;
    padding:10px;
}
.url{
    padding: 10px;
        background-color: rgb(77, 165, 197);
        border: 50px;
        font-weight: bold;
        font-size: 1.15rem;
        border-radius: 50px;
}
.price
{
    padding: 10px;
        background-color: rgb(77, 165, 197);
        border: 50px;
        font-weight: bold;
        font-size: 1.15rem;
        border-radius: 50px;
}

.description{
    padding: 10px;
        background-color: rgb(77, 165, 197);
        border: 50px;
        font-weight: bold;
        font-size: 1.15rem;
        border-radius: 50px;
}
</style>