<template>
     <div>
         <Card v-for="(album,index) in albums" :key='index' 
        :poster='album.poster'
        :title='album.title'
        :author='album.author'
        :year='album.year'/>
     </div>
     
</template>


<script>
import Card from '@/components/Card.vue';

export default {
    name: 'Main',
    components: {
        Card
    },
    props:{
        albums: Array,
    }
}
</script>

<style lang="scss" scoped>
    
</style>
