<template>
    <div id="partners" v-if="partners.length" >
        <b-container>
            <p>PARCEIROS</p>
                <carousel
                    :perPageCustom="[[0, 1],[358,2], [576,3] ,[768, 4]]" 
                    :autoplay="true"
                    :loop=true
                    :autoplayTimeout=5000
                    paginationColor='transparent' 
                    paginationActiveColor='#a67b52'
                    :paginationPadding=0
                > 
                    <slide v-for="partner in partners" :key="partner.id">
                        <span></span>
                            <img :src="partner.image_url" :alt="partner.name">
                    </slide>
                </carousel>        
        </b-container>        
    </div>    
</template>

<script>
    import axios from "axios"
    import { Carousel, Slide } from 'vue-carousel';

export default {
    components: {Carousel,Slide},
    props: {
        link: {type: String},
        header: {type: Array},
    },
    data() {
        return {
            partners: [
                {
                  "id": 1,
                  "name": "Partner #1",
                  "image_url": "https://i.ibb.co/sWtN4WV/partner-one.png"
                },
                {
                  "id": 2,
                  "name": "Partner #2",
                  "image_url": "https://i.ibb.co/vhMPX34/partner-two.png"
                },
                {
                  "id": 3,
                  "name": "Partner #3",
                  "image_url": "https://i.ibb.co/zGfc8Jr/partner-three.png"
                },
                {
                  "id": 4,
                  "name": "Partner #4",
                  "image_url": "https://i.ibb.co/7GkgCZ4/partner-four.png"
                },
                {
                  "id": 5,
                  "name": "Partner #5",
                  "image_url": "https://i.ibb.co/sWtN4WV/partner-one.png"
                },
                {
                  "id": 6,
                  "name": "Partner #6",
                  "image_url": "https://i.ibb.co/vhMPX34/partner-two.png"
                },
                {
                  "id": 7,
                  "name": "Partner #7",
                  "image_url": "https://i.ibb.co/zGfc8Jr/partner-three.png"
                },
                {
                  "id": 8,
                  "name": "Partner #8",
                  "image_url": "https://i.ibb.co/7GkgCZ4/partner-four.png"
                }
            ],
        }
    },

    created() {
        axios.get(this.link)
            .then(response => this.partners = Object.assign([], response.data) )
    }
}
</script>

<style scoped lang="scss">
#partners {
    margin-top:60px;
    margin-bottom:52px;
    padding-top:43px;
    padding-bottom:30px;
    background-color: #f4f4f4;

    .container{
        padding-left:3px;
    }

    p{
        color:#403225;
        font-weight: bold;
        font-size:1.1rem;
        margin-bottom: 50px;
    }

    .VueCarousel{

        /deep/ .VueCarousel-slide{
            vertical-align:middle;

            span{
                display: inline-block;
                height: 100%;
                vertical-align:middle;
            }
        }

        /deep/ .VueCarousel-pagination{
            margin: 25px 0;

            .VueCarousel-dot {
                border: 1px solid #a67b52;
                margin: 1px 9px;
                outline: none;
            }
        }
    }
}

</style>