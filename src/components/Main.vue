<template>
    <div class="bg-container">
        <div class="container">
            <div class="row">
                <!-- richiamiamo il componets (card) importato precedentemente -->
                <!-- con un v-for andiamo a ciclare l'arry del quale siamo in ascolto -->
                <Card class="album-cont" v-for="(album,index) in albums" :key='index' 
                :poster='album.poster'
                :title='album.title'
                :author='album.author'
                :year='album.year'/>
                <!-- inseriamo tutti gli oggetti di cui abbiamo bisogno per il leyout -->
            </div>
        </div>1
    </div>
     
</template>


<script>
import Card from '@/components/Card.vue'; //importiamo il nostro components (card) nel main 

export default {
    name: 'Main',
    components: {
        Card
    },
    props:{ //ci mettiamo in ascolto di app.vue
        albums: Array, //e chiediamo di inviarci un array della chiamata API
    }
}
</script>

<!-- defianiamo lo style valido solo per il main -->

<style lang="scss" scoped>
.bg-container{
    background: #1e2d3b;
    padding: 50px;
    .row{
        .album-cont{
            
            width: calc(100% / 5);
            padding: 20px;
           
        }
    }
}
    
</style>
