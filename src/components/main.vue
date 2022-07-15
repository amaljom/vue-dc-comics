<template>
  <main class="black-band">
    <!-- ci saranno due elementi nel main la fascia nera e quella azzurra -->
    <div class="content-container">
        <h1> Content goes here </h1>
    </div>
    <!-- div azzurro che poi dovò mettere in un altro component -->
    <div class="content-azzurro">
        <ul>
            <li></li>
        </ul>
    </div>
  </main>
</template>

<script>

</script>


<style scoped lang="scss">

.black-band{
    background-color: rgb(26, 25, 25);
    height: 200px;
}
h1{
    color: white;
}
.content-container{
    max-width: 1200px;
    margin: 0 auto;
    display: flex;
    align-items: center;
    height: 100%;
}
</style>
