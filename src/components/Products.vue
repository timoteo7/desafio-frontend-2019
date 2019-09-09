<template>
    <b-container id="products" v-if="products.length">
        <b-row center>
            <b-col v-for="product in products" :key="product[header[0]]">
                <figure>
                    <img :src="product[header[2]]" :alt="product[header[1]]">
                    <figcaption>{{product.name}}</figcaption>
                    <div></div>
                </figure>
            </b-col>
        </b-row>
    </b-container>
</template>

<script>
    import axios from "axios"

export default {
    props: {
        link: {type: String},
        header: {type: Array},
    },

    data() {
        return { products : [
            {
                id:1,
                name:'Curabitor',
                image_url:'https://i.ibb.co/HXTyZjm/curabitor.png',
            },
            {
                id:2,
                name:'Faucibus',
                image_url:'https://i.ibb.co/CbGgpgP/faucibus.png',
            },
            {
                id:3,
                name:'Ullamcorper',
                image_url:'https://i.ibb.co/Np5d4tj/ullamcorper.png',
            },
            {
                id:4,
                name:'Duis Libero',
                image_url:'https://i.ibb.co/pxg91sD/duislibero.png',
            },
            {
                id:5,
                name:'Pellentesque',
                image_url:'https://i.ibb.co/g6ygK0y/pellentesque.png',
            },
        ] }
    },

    created() {
        axios.get(this.link)
                .then(response => this.products = Object.assign([], response.data) )
    }
}
</script>

<style scoped lang="scss">

#products{
    margin-top: -5.65%;

    .row{
        flex-wrap: nowrap;
        margin-right: -4px;
        margin-left: -3px;

        .col{
            margin:0;
            margin-right: -1px;
            margin-left: -1px;
            padding:0px;
            overflow:hidden;

            figure{
                margin:0;
            
                img{
                    width: 100%;
                }

                figcaption{
                    position: absolute;
                    bottom: 1.4rem;
                    color:#939393;
                    font-size:8px;
                    @media (min-width:576px) { font-size:11px;}
                    @media (min-width:992px) { font-size:19px;}
                    font-family: 'Montserrat-Black', sans-serif;
                    font-weight: 900;
                    width:100%;
                    text-transform:uppercase;
                    z-index: 1;
                }

                &:hover figcaption{
                    color:white;
                }

                div{
                    background:linear-gradient(to bottom , lightgrey 40%,black);
                    position: absolute;
                    width: 100%;
                    height: 100%;
                    top:0;
                    opacity: 0.75;
                }

                &:hover div{
                    background:linear-gradient(to bottom , Transparent 50%,black);
                }
            }
        }
    }
}

</style>
