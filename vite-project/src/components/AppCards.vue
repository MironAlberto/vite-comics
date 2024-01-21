<script>
export default{
    data(){
        return{

        };
    },
    props:{
        thumbs: String,
        series: String
    }
}
</script>

<template>
    <div class="card">
        <div class="thumbnail">
            <img :src="thumbs" :alt="series">
        </div>

        <h5>
            {{ series }}
        </h5>
    </div>
</template>

<style lang="scss" scoped>
    .card{
        width: calc(100% / 6);
        
        img{
            width: 100%;
            height: 270px;
            padding: 10px;
        }

        h5{
            text-align: center;
            text-transform: uppercase;
        }
    }
</style>