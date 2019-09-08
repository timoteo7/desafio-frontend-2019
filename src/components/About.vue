<template>
    <b-container>
        <b-row>
            <b-col sm="5">
                <div id="inner">
                    <img src="../assets/about.jpg" alt="image">
                </div>
            </b-col>
        
            <b-col id='about' sm="7">
                <h1>SOBRE A BAKERY</h1>
                <div >
                    <p>
                        Ut vitae volutpat risus. Nam vitae congue odio, mattis 
                        dignissim neque. Nam eros sapien, semper in 
                        pellentesque ut, suscipit eu nunc. Donec malesuada
                        egestas ligula, non malesuada sapien suscipit ut.
                    </p>
                    <p>
                        Praesent sed ipsum ullamcorper purus scelerisque
                        laoreet. Nulla lobortis ex eu mi accumsan, non
                        hendrerit ex rhoncus. Etiam auctor libero porttitor
                        tellus imperdiet consequat. Nam porttitor diam in
                        eleifend fringilla.
                    </p>
                </div>
                <div>
                    <a href="#">Conheça mais <img src="../assets/long-arrow-right.svg" /></a> 
                </div>
            </b-col>
        </b-row>
    </b-container>
</template>

<style scoped lang="scss">

.container{
    margin-top: 38px;

    #inner{
        position: absolute;
        overflow: hidden;
        height: 311px;
        width:265px;
        margin:0;
        padding:0;

        img{
            position: absolute;
            top:-0.7%;
            left: -21%;
            height:322px;
        }
    }

    .col-sm-5 {
        padding: 0px 10px;
    }

    #about{
        padding-right: 45px;
        padding-left: 26px;
        text-align: left;
        color: #484848;
        font-size: .96rem;
        font-weight: 100;
        

        h1{
            font-size: 18px;
            font-weight: 700;
            margin-bottom: 1.2rem;
        }
        
        a{
            color: #a67b52;
            img{ height:14px; }
        }
    }
}
</style>

