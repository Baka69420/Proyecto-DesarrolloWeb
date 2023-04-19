<template>
    <div id="title">
        <h1>Deliciosos productos</h1>
    </div>

    <video id="quality-product" width="500" height="500" controls autoplay muted>
        <source src="@/assets/videos/product-quality.mp4" type="video/mp4">
    </video>

</template>



<style scoped>
#title {
    color: #ffa753;
    text-align: center;
    border-bottom: 2px solid #ffa753;
    margin-bottom: 20px; 
}

#quality-product {
    display: block;
    max-width: 80%;
    height: 20%;
    margin: 0 auto;
}
</style>