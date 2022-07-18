<template>

    <li >
        <img :src="require(`../assets/buy${img}`)" alt="text">
        <p class="text-style">{{ text}}</p>
    </li>
    
</template>

<script>

export default {
    props:{
        img:String,
        text:String
    }
}

</script>

<style>

li{
    padding: 0 30px;
    display: flex;
    align-items: center;
}
img{
        width: 56px;
        height: 62px;
}
.text-style{
    font-size: 17px;
    color: white;
    padding-left: 12px;
}

</style>