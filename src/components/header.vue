<template>
<!-- CREO UN DIV DOVE METTERE L'HEADER -->
<!-- ALL' INTERNO DI ESSO CREO DUE DIV CONTENTI RISPETTIVAMENTE LOGO E LA LISTA -->
  <header>
        <nav class="navbar">
            <!-- logo -->
            <div>
                <img src="../assets/dc-logo.png" alt="Non trovato">
            </div>
            <!-- lista -->
            <div>
                <ul>
                    <li v-for="(element,index) in listElementForNavbar" :key="index">{{  element.text }}</li>
                </ul>
            </div>
        </nav>
  </header>
</template>

<script>

export default{
    data: function(){
        return{
            listElementForNavbar:[
                        {
                            text: 'CHARACTERS'
                        },
                        {
                            text: 'COMICS'
                        },
                        {
                            text: 'MOVIES'
                        },
                        {
                            text: 'TV'
                        },
                        {
                            text: 'GAMES'
                        },
                        {
                            text: 'COLLECTIBLES'
                        },
                        {
                            text: 'VIDEOS'
                        },
                        {
                            text: 'FANS'
                        },
                        {
                            text: 'NEWS'
                        },
                        {
                            text: 'SHOP'
                        }
                    ]
        }
    }
}
   
</script>


<style lang="scss" scoped>
 .navbar{
    margin-top: 1.5rem;
    display: flex;
    justify-content: space-around;
 }

 ul li{
    display: inline;
    list-style: none;
    padding: 1rem;
    font-size: 0.9rem

}
 
 img{
    width: 80px;
 }

</style>