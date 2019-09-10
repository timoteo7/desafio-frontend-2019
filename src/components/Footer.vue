<template>
    <div id="fundo">
        <b-container>
            <b-row>
                <b-col>
                    <img id="logo" src="../assets/logo.svg" alt="logo">
                    <div>
                        <a href="#"><font-awesome-icon :icon="['fab', 'twitter-square']" size='lg'/></a>
                        <a href="#"><font-awesome-icon :icon="['fab', 'google-plus-square']" size='lg'/></a>
                        <a href="#"><font-awesome-icon :icon="['fab', 'facebook-square']" size='lg'/></a>
                    </div>
                </b-col>

                <b-col>
                    <div>HOME</div>
                    <div>SOBRE</div>
                    <div>RECEITAS</div>
                    <div>NOTÍCIAS</div>
                    <div>CONTATO</div>
                </b-col>

                <b-col>
                    <div>
                        <div>
                            <i></i>
                            <p>CONTATO</p>
                            <div >(99) 9999-9999  |  (99) 99999-9999</div>
                        </div>
                        <div>
                            <i></i>
                            <p> LOCALIZAÇÃO</p>
                            <div>Nam porttitor diam in eleifend fringilla, 3180</div>
                        </div>
                    </div>
                </b-col>
            </b-row>

            <div>
                <div >
                        <div>© Bakery 2017. Todos direitos reservados.</div>
                </div>
                <div>
                    <div><img src="../assets/ow.png" alt="ow"></div>
                </div>
            </div>
        </b-container>
    </div>
    
</template>

<style scoped lang="scss">

#fundo{
    background-color:#403225;
    padding:49px 0;
}

.row{
    margin: 0 20px;
    font-size: 14px;
    color:white;

    .col:first-child{
        img{
            height:112px;
            margin-bottom:20px;
        }

        a{
            color: #a67b52;
            padding: 0 .7rem;
        }
    }

    .col:nth-child(2){
        border-left: 1px rgb(134, 127, 121) solid;
        border-right: 1px rgb(134, 127, 121) solid;
    }

    .col:last-child{
        text-align: left;
        font-size: 12px;

        p{
            font-weight: 900;
        }
    }
}

</style>

