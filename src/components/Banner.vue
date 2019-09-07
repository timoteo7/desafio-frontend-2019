<template>
        <carousel 
            :per-page=1
            :autoplay=true
            :loop=true
            :autoplayTimeout=5000
            paginationPosition='bottom-overlay' 
            paginationColor='transparent' 
            paginationActiveColor='white'
            :paginationPadding=0
        > 

            <slide v-for="banner in banners" :key="banner[header[0]]">
                <img :src="banner[header[2]]" :alt="banner[header[1]]">
            </slide>
        </carousel>
</template>

<script>
    //import axios from "axios"
    import { Carousel, Slide } from 'vue-carousel';

export default {
    components: {Carousel,Slide},
    props: {
        link: {type: String},
        header: {type: Array},
    },

    data() {
        return { 
            banners : [
                {
                    id:1,
                    title:'Banner #1',
                    image_url:'https://i.ibb.co/cwQGNwG/banner-1.png',
                },
                {
                    id:2,
                    title:'Banner #2',
                    image_url:'https://i.ibb.co/jHq1pZR/banner-2.png'
                },
                {
                    id:3,
                    title:'Banner #3',
                    image_url:'https://i.ibb.co/3v3TkwF/banner-3.png'
                },
            ] 
        }
    },

    mounted(){
        //axios.get(this.link)
                //.then(response => this.banners = Object.assign([], response.data) )
    },
}
</script>


<style lang="scss">

.VueCarousel{
    margin-top: 8px;

    .VueCarousel-slide{
        img{
            width: 100%;
        }
    }

    .VueCarousel-pagination{
        bottom: 32%!important;
        @media not all and(min-width:768px) { display:none;}

        .VueCarousel-dot{
            border: 1px solid white!important;
            margin: 1px 9px;
            outline: none!important;
        }
    }
}

</style>