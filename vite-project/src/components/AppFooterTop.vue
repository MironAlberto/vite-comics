<script>
export default {
    data() {
        return {
            footerLinks: [
                {
                    image: "buy-comics-digital-comics.png",
                    text: "DIGITAL COMICS"
                },
                {
                    image: "buy-comics-merchandise.png",
                    text: "DC MERCHANDISE"
                },
                {
                    image: "buy-comics-subscriptions.png",
                    text: "SUBSCRIPTION"
                },
                {
                    image: "buy-comics-shop-locator.png",
                    text: "COMIC SHOP LOCATOR"
                },
                {
                    image: "buy-dc-power-visa.svg",
                    text: "DC POWER VISA"
                },
            ]
        };
    },
    methods: {
        footerImage(image){
            return new URL(`../../public/img/${image}`, import.meta.url).href
        }
    }
}
</script>

<template>
    <footer class="footer-top">
        <ul>
            <li v-for="(elem, index) in footerLinks" :key="index">
                <div class="image">
                    <img :src="footerImage(elem.image)" alt="">
                </div>
                <div class="text">
                    {{ elem.text }}
                </div>
            </li>
        </ul>
    </footer>
</template>

<style lang="scss" scoped>
.footer-top{
    width: 100%;
    background-color: #0282F9;
    color: white;
    display: flex;
    justify-content: center;
    align-items: center;

    ul{
        list-style-type: none;
        display: flex;
        
    }

    li{
        display: flex;
        padding: 50px 50px 40px 0px;

        .image{
            width: 55px;

            img{
                width: 100%;
                height: 100%;
                object-fit: contain;
            }
        }
        
        .text{
            line-height: 85px;
            padding-left: 12px;
            align-items: center;
        }
    }
}
</style>