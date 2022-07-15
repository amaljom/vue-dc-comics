<template>
  <main>
    <!-- ci saranno due elementi nel main la fascia nera e quella azzurra -->
    <div class="container black-band">
        <div class="content-container posizionamento-elementi">
            <h1> Content goes here </h1>
        </div>
        <!-- div azzurro che poi dovò mettere in un altro component -->
        <div class="content-azzurro ">
            <div class="posizionamento-elementi">
                <ul>
                    <li v-for="(image,index) in listImagesForBlueBand" :key="index"><img :src="image.image" alt="NON TROVATO"></li>
                </ul>
            </div>
            
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
                            image: '../assets/buy-comics-digital-comics.png'
                        },
                        {
                            image: '../assets/buy-comics-merchandise.png'
                        },
                        {
                            image: '../buy-comics-shop-locator.png'
                        },
                        {
                            image: '../assets/buy-comics-subscriptions.png'
                        },
                        {
                            image: '../assets/buy-dc-power-visa.svg'
                        }
                       
                    ]
        }
    }
}

</script>


<style scoped lang="scss">

.black-band{
    background-color: rgb(26, 25, 25);
    height: 200px;
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
.content-azzurro{
    height: 250px;
    background-color: rgb(0, 178, 238);
}
</style>
