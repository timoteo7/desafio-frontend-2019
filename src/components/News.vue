<template>
    <div id="news">
        <div >ÚLTIMAS NOTÍCIAS</div>
        
        <div v-for="New in news" :key="New[header[0]]" >
            <div >{{ New[header[2]] }}</div>
            <div >{{ New[header[1]] }}</div>
            <hr>
        </div>

        <div >
            <a href="#">Lista Completa <i></i></a>
        </div>
    </div>
</template>



<script>
    import axios from "axios"

export default {
    props: {
        link: {type: String},
        header: {type: Array},
    },
    data() {
        return {
            news: []
        }
    },

    mounted() {
        axios.get(this.link)
            .then(response => this.news = Object.assign([], response.data) )
    }
}
</script>

<style socped lang="scss">

#news{
    background-color: #fafafa;
}

</style>