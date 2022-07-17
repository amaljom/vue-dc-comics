<template>
  <main>
    <!-- ci saranno due elementi nel main la fascia nera e quella azzurra -->
    <div class="container black-band">
        <div class="content-container posizionamento-elementi">
            <h1> Content goes here </h1>
        </div>
    </div>
    <!-- div azzurro che poi dovò mettere in un altro component -->
    <div class="content-azzurro ">
            <div class="posizionamento-elementi content-container content-container-images">
                <ul>
                    <li v-for="(item, index) in listImagesForBlueBand" :key="index">
                        <img :src="`../assets/buy${item.image}`" alt="non trovato">
                        <p class="text-style">{{ item.textImage}}</p>
                    </li>
                </ul>
            </div>
        </div>
  </main>
</template>

<script>
export default{
    data: function(){
        return{
            listImagesForBlueBand:[
                        {
                            image: '-comics-digital-comics.png',
                            textImage: 'Digital comics'
                        },
                        {
                            image: '-comics-merchandise.png',
                            textImage: 'DC Merchandise'
                        },
                        {
                            image: '-comics-subscriptions.png',
                            textImage: 'subscription'
                        },
                        {
                            image: '-comics-shop-locator.png',
                            textImage: 'Comics shop locator'
                        },
                        {
                            image: '-dc-power-visa.svg',
                            textImage: 'DC power visa'
                        }
                    ]
        }
    }
}
</script>


<style scoped lang="scss">
.black-band{
    background-color: rgb(26, 25, 25);
    height: 170px;
}
.content-azzurro{
    height: 210px;
    background-color: rgb(0, 178, 238);
}
h1{
    color: white;
}
.posizionamento-elementi{
    max-width: 1200px;
    margin: 0 auto;
}
.content-container{
    display: flex;
    align-items: center;
    height: 100%;
}
.content-container-images{
    justify-content: center;
}
ul{
    display: flex;
    list-style: none;
}
ul li{
    padding: 0 40px;
    display: flex;
    align-items: center;
}
img{
        width: 56px;
        height: 62px;
}
.text-style{
    font-size: 25px;
    color: white;
    padding-left: 15px;
}
main{
    position: relative;
    z-index: 50;
}
</style>
