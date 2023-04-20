<script>
export default {
    props: {
      productID: String
    },
    data(){
        return {
            product: {},
            cantidad: 1
        }
    },
    methods: {
        obtenerProducto(){
            fetch("https://baka69420.github.io/Proyecto-DesarrolloWeb/api/products.json").then(response => {
                if(response.ok) return response.json();
            }).then(json => {
                let item = json.find(e => {return this.productID == e['id']});
                if(item) this.product = item;
                else this.product = { error: true };
            })
        }
    },
    beforeMount(){
        this.obtenerProducto();
    }
}
</script>

<template>
    <div id="title">
        <h1>Detalles de Producto</h1>
    </div>
    <div id="info-producto">
        <div id="detalles">
            <div class="product" :key="product['id']">
                <img :src="product['img-url']" :alt="'Photo of' + product['name']">
                <div id="text">
                    <h5>{{ product['name'] }}</h5>
                    <p>{{ product['description'] }}</p>
                </div>
            </div>
        </div>
        <div id="costo">
            <div class="product" :key="product['id']">
                <div id="text">
                    <h5>Costo: {{ product['cost'] }}</h5>
                    <form>
                        <label for="cantidad"> Cantidad:</label>
                        <input :value="cantidad" name="cantidad" type="number">
                        <button type="submit">Agregar al carrito</button>
                    </form>
                </div>
            </div>
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

    #info-producto{
        display: flex;
        gap: 10px;
    }

    #info-producto #detalles {
        flex-basis: 70%;
        flex-grow: 1;
    }

    #info-producto #costo {
        flex-basis: 30%;
        flex-grow: 1;
    }

    input, button {
        width: 100%;
    }

    .product {
        height: fit-content;
        width: 100%;
        word-wrap: normal;
        text-overflow: ellipsis;
        overflow: hidden;
        border: black solid 1px;
        padding: 10px;
        border-radius: 10px;
        background-color: #fecb70;
    }

    .product #text h5, .product #text p {
        text-overflow: ellipsis;
        white-space: wrap;
        word-wrap: normal;
        margin-bottom: 0;
    }

    .product #text h5 {
        margin-bottom: 10px
    }

    .product img {
        height: 50%;
        width: 50%;
        display: block;
        border-radius: 100%;
        margin: 0 auto;
        margin-bottom: 20px;
    }

    form button {
        display: block;
        background-color: #ffa753;
        border-radius: 10px;
        width: 80%;
        height: 40px;
        margin: 10px auto;
    }
</style>