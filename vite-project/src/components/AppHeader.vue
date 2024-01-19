<script>
export default {
    data() {
        return {
            selectedNav: 0,
            navBar: [
                {
                    nav: 'CHARACTERS'
                },
                {
                    nav: 'COMICS'
                },
                {
                    nav: 'MOVIES'
                },
                {
                    nav: 'TV'
                },
                {
                    nav: 'GAMES'
                },
                {
                    nav: 'COLLECTIBLES'
                },
                {
                    nav: 'VIDEOS'
                },
                {
                    nav: 'FANS'
                },
                {
                    nav: 'NEWS'
                },
                {
                    nav: 'SHOP'
                },
            ],
        };
    },
    methods: {
        activeClass(i){
            if(this.selectedNav == i){
                return 'active';
            }
            else{
                return '';
            }
        },
        switchActive(i){
            this.selectedNav = i;
        },
    }
}
</script>

<template>
    <header>
        <div class="container">
            <div>
                <img src="/img/dc-logo.png" alt="dc-logo">
            </div>
            <div>
                <ul>
                    <li v-for="(elem, i) in navBar" :key="i">
                        <span class="nav-size" :class="activeClass(i)" @click="switchActive(i)">
                            {{ elem.nav }}
                        </span>
                    </li>
                </ul>
            </div>
        </div>
    </header>
</template>

<style lang="scss" scoped>
header{
    width: 100%;
    background-color: white;
    
    
    .container{
        max-width: 1200px;
        margin: 0 auto;
        display: flex;
        justify-content: space-between;
        align-items: center;

        ul{
            list-style-type: none;

            li{
                color: white;
                display: inline-block;
                
                .nav-size{
                    margin-left: 30px;
                    font-size: small; 
                    font-weight: bold;
                    cursor: pointer;
                    color: black;
                }

                .active{
                    border-bottom: 4px solid #0282F9;
                    padding-bottom: 50px;
                    color: #0282F9;
                }
            }
        }
    }
    

    img{
        width: 80px;
        padding: 20px 0;
    }
}
</style>