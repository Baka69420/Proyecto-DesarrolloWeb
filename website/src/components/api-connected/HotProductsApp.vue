<script>
    export default {
        data(){
            return {
                hotitems: [],
                products: []
            }
        },
        methods: {
            obtenerHotItems(){
                fetch("https://baka69420.github.io/Proyecto-DesarrolloWeb/api/products.json").then(response => {
                    if(response.ok) return response.json();
                }).then(json => {
                    this.products = json;
                }).then(() => {
                    fetch("https://baka69420.github.io/Proyecto-DesarrolloWeb/api/hot-products.json").then(response => {
                        if(response.ok) return response.json();
                    }).then(json => {
                        for(let item of json){
                            let hotitem = this.products.find(e => {return item['id'] == e['id']});
                            if(hotitem) this.hotitems.push(hotitem);
                        }
                    })
                })
            }
        },
        beforeMount(){
            this.obtenerHotItems();
        }
    }
</script>

<template>
    <div id="title">
        <h1>Mejores productos</h1>
    </div>
    <div id="products">
        <div v-for="product in hotitems" class="product" :key="product['id']">
            <img :src="product['img-url']" :alt="'Photo of' + product['name']">
            <div id="text">
                <h5>{{ product['name'] }}</h5>
                <p>Costo: {{ product['cost'] }}</p>
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

#products {
    width: 100%;
    height: auto;
    display: flex;
    gap: 5px;
    flex-wrap: wrap;
}

#products .product {
    flex-basis: 100%;
    height: fit-content;
    word-wrap: normal;
    text-overflow: ellipsis;
    overflow: hidden;
    border: black solid 1px;
    padding: 10px;
    border-radius: 10px;
    background-color: #fecb70;
    display: flex;
    flex-direction: row;
    gap: 20px;
}

#products .product * {
    display: block;
    margin: auto 0;
}


#products .product #text h5, #products .product #text p {
    text-overflow: ellipsis;
    word-wrap: normal;
}

#products .product img {
    height: 100px;
    width: 100px;
    display: block;
    border-radius: 100%;
}
</style>