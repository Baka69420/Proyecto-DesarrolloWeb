<template>
    <div id="carouselId" class="carousel slide" data-bs-ride="carousel">
        <div class="carousel-inner" role="listbox">
            <div class="carousel-item" v-for="item, key in images" :key="key" :class="key==0 ? 'active' : ''">
                <img :src="item['img-url']" class="w-100 d-block">
                <div class="carousel-caption d-none d-md-block">
                    <h1>{{ item["title"] }}</h1>
                    <p v-if="item['descripcion'] != ''">{{ item["descripcion"] }}</p>
                </div>
            </div>
        </div>
        <button class="carousel-control-prev" type="button" data-bs-target="#carouselId" data-bs-slide="prev">
            <span class="carousel-control-prev-icon" aria-hidden="true"></span>
            <span class="visually-hidden">Previous</span>
        </button>
        <button class="carousel-control-next" type="button" data-bs-target="#carouselId" data-bs-slide="next">
            <span class="carousel-control-next-icon" aria-hidden="true"></span>
            <span class="visually-hidden">Next</span>
        </button>
    </div>
</template>

<script>
    export default {
        data(){
            return {
                images: []
            }
        },
        methods: {
            obtenerImagenes(){
                fetch("https://baka69420.github.io/Proyecto-DesarrolloWeb/api/carousel-api.json").then(response => {
                    if(response.ok) return response.json();
                }).then(json => {
                    this.images = json;
                })
            }
        },
        beforeMount(){
            this.obtenerImagenes();
        }
    }
</script>

<style>
#carouselId{
    width: 100%;
    height: auto;
}

.carousel-item {
    text-align: center;
}
</style>