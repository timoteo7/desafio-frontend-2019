<template>
    <div id="news">
        <h1>ÚLTIMAS NOTÍCIAS</h1>
        <div v-for="New in news" :key="New[header[0]]" >
            <p>{{ New[header[2]] }}</p>
            <div id="short">{{ New[header[1]] }}</div>
            <hr>
        </div>
        <div id="link">
            <a href="#">Lista Completa <img src="../assets/long-arrow-right.svg" /></a>
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
            news: [
                {
                  "id": 1,
                  "author": "Luke Barnes",
                  "title": "Facebook cares about their users\u2019 privacy*",
                  "description": "Facebook cares about privacy. Or at least is says it does. After two-and-a-half years bouncing from one scandal and misstep to another (most notably with Cambridge Analytica, where Facebook\u2019s lax attitude towards user privacy led to nearly 100 million users\u2019 \u2026",
                  "published_at": "2019-07-30T16:04:42Z",
                  "content": "Facebook cares about privacy. Or at least is says it does.\r\nAfter two-and-a-half years bouncing from one scandal and misstep to another (most notably with Cambridge Analytica, where Facebook\u2019s lax attitude towards user privacy led to nearly 100 million users\u2019\u2026 [+3810 chars]"
                },
                {
                  "id": 2,
                  "author": "Osato Avan-Nomayo",
                  "title": "Was Tether the Unknown Bitcoin Whale Behind Monday\u2019s $2.27 Billion Transfer?",
                  "description": "The massive $2.27 billion bitcoin transfer that occurred on Monday has led to the emergence of fanciful theories that Tether might be creating a private dark pool for future USDT issuance. The Facts: Bitcoin Whale Moves $2.27 Billion in Six Hours Monday (July\u2026",
                  "published_at": "2019-07-30T16:00:14Z",
                  "content": "The massive $2.27 billion bitcoin transfer that occurred on Monday has led to the emergence of fanciful theories that Tether might be creating a private dark pool for future USDT issuance.\r\nThe Facts: Bitcoin Whale Moves $2.27 Billion in Six Hours\r\nMonday (Ju\u2026 [+2513 chars]"
                },
                {
                  "id": 3,
                  "author": "Arizona Republic, Jeannette Hinkle, Arizona Republic",
                  "title": "How 4 IT technicians saved an Arizona hospital from hacker ransomware",
                  "description": "Hackers are asking for, and getting, higher ransoms in attacks. Wickenburg Community Hospital didn't pay.",
                  "published_at": "2019-07-30T16:00:14Z",
                  "content": "A team of four IT professionals saved Wickenburg Community Hospital from paying a ransom to hackers.\r\n (Photo: Jeannette Hinkle /The Republic)\r\nMike Nelson often comes to work early, around 6 a.m., so it was Nelson who first discovered the message.\r\nNelson, an\u2026 [+8473 chars]"
                }
            ]
        }
    },

    created() {
        axios.get(this.link)
            .then(response => this.news = Object.assign([], response.data) )
    }
}
</script>

<style socped lang="scss">

#news{
    //background-color: grey;
    padding: 2.4rem 2rem;
    margin: 0 8px;
    text-align: left;
    background-color: #fafafa;

    h1{
        color: #d1bba6;
        font-size: 18px;
        font-weight: 700;
        margin-bottom: 1.4rem;
    }

    p{
        color: #a67b52;
        font-size: 11px;
        font-weight: 700;
        margin-bottom: 0.1rem;
    }

    #short{
        color: #484848;
        font-size: 14px;
        font-weight: 100;
    }

    #link{
        text-align: right;

        a{
            color: #a67b52;

            img{
                height:14px;
            }
        }
    }
}

</style>