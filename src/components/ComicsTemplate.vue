<template>
        <div class="width-img-wrapper">
            <img class="img-wrapper" :src="img" alt="">
            <p>{{ series }}</p>
        </div>
</template>

<script>
export default {

    props:{
        img: String,
        series: String,
        price: Number,
        type: String
    }
}
</script>

<style>
.img-wrapper{
    height: 180px;
    width: 170px;
    padding: 8px 0px;
}
.width-img-wrapper{
    width: calc( 100% / 6);
}
</style>