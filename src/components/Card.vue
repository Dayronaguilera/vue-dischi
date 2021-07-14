<template>
    <div class="card-container">
        <div class="contanier">
            <img :src="poster" :alt="`image of ${title}`" />
            <div class="title">{{title}}</div>
            <div class="author">{{author}}</div>
            <div class="year">{{year}}</div>
        </div>
    </div>    
</template>


<script>
export default {
    name: 'Card',
    props:{
        poster: String,
        title: String,
        author: String,
        year: String
    }
}
</script>

<style lang="scss" scoped>
    .card-container{
        text-align: center;
        background:rgb(14, 60, 104);
        color:white;
        .contanier{
            padding: 15px;
            img{
                width: 100%;
            }
            .title{
                font-size: 25px;
            }
            .author{
                color: grey;
            }
            .year{
                 color: grey;
            }

        }
    }
    
</style>
