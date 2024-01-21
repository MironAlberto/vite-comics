<script>
export default {
    data() {
        return {
            footerBottomLinks: {
                dcComics: [
                    "DC COMICS",
                    {
                        text: 'Characters'
                    },
                    {
                        text: 'Comics'
                    },
                    {
                        text: 'Movies'
                    },
                    {
                        text: 'TV'
                    },
                    {
                        text: 'Games'
                    },
                    {
                        text: 'Videos'
                    },
                    {
                        text: 'News'
                    },
                ],
                dc: [
                    "DC",
                    {
                        text: 'Terms of Use'
                    },
                    {
                        text: 'Privacy policy (New)'
                    },
                    {
                        text: 'Ad Choices'
                    },
                    {
                        text: 'Advertising'
                    },
                    {
                        text: 'Jobs'
                    },
                    {
                        text: 'Subscriptions'
                    },
                    {
                        text: 'Talent Workshops'
                    },
                    {
                        text: 'CPSC Certificates'
                    },
                    {
                        text: 'Ratings'
                    },
                    {
                        text: 'Shop Help'
                    },
                    {
                        text: 'Contact Us'
                    },
                ],
                sites: [
                    "SITES",
                    {
                        text: 'DC'
                    },
                    {
                        text: 'MAD Magazine'
                    },
                    {
                        text: 'DC Kids'
                    },
                    {
                        text: 'DC Universe'
                    },
                    {
                        text: 'DC Power Visa'
                    },
                ],
                shop: [
                    "SHOPS",
                    {
                        text: 'Shop DC'
                    },
                    {
                        text: 'Shop DC Collectibles'
                    },
                ]
            },
            socialNetworkLinks: [
                {
                    image: 'footer-facebook.png'
                },
                {
                    image: 'footer-twitter.png'
                },
                {
                    image: 'footer-youtube.png'
                },
                {
                    image: 'footer-pinterest.png'
                },
                {
                    image: 'footer-periscope.png'
                }
            ]

            
        };
    },
    methods: {
        footerLinkImages(image){
            return new URL(`../../public/img/${image}`, import.meta.url).href
        }
    }
}
</script>

<template>
    <footer class="footer-bottom">
        <div class="links">
            <div  v-for="(elem, index) in footerBottomLinks" :key="index">
                <h3>
                    {{ elem[0] }}
                </h3>
                <div>
                    <ul>
                        <li v-for="(elem, index) in elem.slice(1)" :key="index">
                            {{ elem.text }}
                        </li>
                    </ul>
                </div>
            </div>
        </div>
        <div class="footer-bottom-image">
                
        </div>
    </footer>
    <footer class="footer-links">
        <div class="container">
            <div class="button">
                <button>
                    <strong>
                        SIGN-UP NOW!
                    </strong>
                </button>
            </div>
            <div class="social-networks">
                <div class="follow-us">
                    <h3>
                        FOLLOW US
                    </h3>
                </div>
                <div class="social-links">
                    <ul>
                        <li v-for="(link, index) in socialNetworkLinks" :key="index">
                            <img :src="footerLinkImages(link.image)" alt="">
                        </li>
                    </ul>
                </div>
            </div>
        </div>
    </footer>
</template>

<style lang="scss" scoped>
.footer-bottom{
    width: 100%;
    height: 380px;
    background-image: url(../../public/img/footer-bg.jpg);
    background-size: cover;
    color: white;
    display: flex;
    justify-content: space-around;
    align-items: center;

    .links{
        display: flex;
        padding-left: 300px;

        h3{
            padding-left: 30px;
            padding-bottom: 12px;
        }

        ul{
        list-style-type: none;
        padding-left: 30px;

            li{
                color: #73776E;
            }
                
        }
    }

    .footer-bottom-image{
        width: 100%;
        height: 100%;
        background-image: url(../../public/img/dc-logo-bg.png);
        background-repeat: no-repeat;
        background-position: center;
        
    }
}

.footer-links{
    width: 100%;
    height: 158px;
    background-color: #303030;
    
    .container{
        max-width: 1200px;
        margin: 0 auto;
        display: flex;
        justify-content: space-between;
        align-items: center;
        padding-top: 60px;

        button{
        padding: 10px;
        border: 2px solid #0282F9;
        background-color: #303030;
        color: white;
        cursor: pointer;
        }

        .social-networks{
            display: flex;
            justify-content: space-between;

            h3{
                color: #0282F9;
                padding-right: 30px;
                padding-top: 8px;
            }

            ul{
                list-style: none;

                li{
                    display: inline-block;
                    padding-left: 10px;
                }
            }
        }
    }

}
</style>