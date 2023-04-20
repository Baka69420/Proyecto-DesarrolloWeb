<script>
import router from '@/router';

    export default {
        data(){
            return {
                products: []
            }
        },
        methods: {
            obtenerProductos(){
                fetch("https://baka69420.github.io/Proyecto-DesarrolloWeb/api/products.json").then(response => {
                    if(response.ok) return response.json();
                }).then(json => {
                    this.products = json;
                })
            },
            verProducto(productoID){
                router.push({name:'product', params:{ productID: productoID }});
            }
        },
        beforeMount(){
            this.obtenerProductos();
        }
    }
</script>

<template>
    <div id="title">
        <h1>Todos los productos</h1>
    </div>
    <div id="products">
        <div v-for="product in products" v-on:click="verProducto(product['id'])"  class="product" :key="product['id']">
            <img :src="product['img-url']" :alt="'Photo of' + product['name']">
            <h5>{{ product['name'] }}</h5>
            <p>Costo: {{ product['cost'] }}</p>
        </div>
    </div>
</template>

<style scoped>
#title {
    color: #ffa753;
    text-align: center;
    border-bottom: 2px solid #ffa753;
    margin-bottom: 20px; 
}

#products {
    width: 100%;
    height: auto;
    display: flex;
    gap: 5px;
    flex-wrap: wrap;
}

#products .product {
    flex-grow: 1;
    flex-shrink: 0;
    height: fit-content;
    word-wrap: normal;
    text-overflow: ellipsis;
    overflow: hidden;
    border: black solid 1px;
    padding: 10px;
    border-radius: 10px;
    background-color: #fecb70;
}

#products .product h5, #products .product p {
    text-overflow: ellipsis;
    white-space: nowrap;
    word-wrap: normal;
    margin-bottom: 0;
}

#products .product img {
    height: 150px;
    width: 150px;
    display: block;
    border-radius: 100%;
    margin: 0 auto;
    margin-bottom: 20px;
}

@media only screen and (max-width: 575px) {
    #products .product {
        flex-basis: 100%;    
    }
}

@media only screen and (min-width: 575px) and (max-width: 1000px) {
    #products .product {
        flex-basis: 45%;    
    }
}

@media only screen and (min-width: 1000px) {
    #products .product {
        flex-basis: 30%;    
    }
}
</style>