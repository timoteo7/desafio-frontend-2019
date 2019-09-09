<template>
    <b-container id='contact'>
        <p class="text-left">CONTATO</p>
        <div class="text-left">Ut vitae volutpat risus. Nam vitae congue odio, mattis dignissim neque. Nam eros sapien, semper in pellentesque ut, suscipit eu nunc. Donec malesuada egestas ligula, non malesuada sapien suscipit ut. </div>
        <b-row>
            <b-col sm='6'>
                <div>
                    <label for="name">Nome*</label>
                    <input type="text"
                        id="name" name="name"
                        placeholder="Nome"
                        :model="form.name"
                        required>
                </div>

                <div>
                    <label for="email">E-mail*</label>
                    <input type="email"
                        id="email" name="email"
                        placeholder="E-mail"
                        :model="form.email" 
                        required>
                </div>
                <div>
                    <label for="city">Cidade</label>
                    <input type="text"
                        id="city" name="city"
                        :model="form.city" 
                        placeholder="Cidade">
                </div>
                <div>
                    <label for="phone">Telefone*</label>
                    <input type="text"
                        id="phone" name="phone"
                        :model="form.phone"
                        v-mask="'(##) ########'"
                        placeholder="(99) 99999999"
                        required>
                </div>
            </b-col>
            <b-col sm='6'>
                <div>
                    <label for="subject">Assunto*</label>
                    <input type="text"
                        id="subject" name="subject"
                        :model="form.subject" 
                        placeholder="Assunto"
                        required>
                </div>
                <div>
                    <label for="message">Mensagem*</label>
                    <textarea id="message" name="message"
                        :model="form.message"
                        placeholder="Digite aqui sua mensagem..."
                        required>
                    </textarea>
                </div>
            </b-col>
        </b-row>
        <button>Enviar</button>
    </b-container>
</template>


<script>
import {mask} from 'vue-the-mask'

export default {
    directives: {mask},
    data() {
        return {
            form: {
                name: '',
                email: '',
                city: '',
                phone: '',
                subject: '',
                message: ''
            },
        }
    },
}
</script>

<style scoped lang="scss">

#contact{
    font-family: 'Montserrat-Regular', sans-serif;
    padding-left:9px;
    font-size: 13.4px;
    font-weight: 300;
    text-align:right;
    margin-bottom:57px;

    p{
        font-size: 18px;
        font-weight: 700;
        margin-bottom:10px;
    }

    .row{
        margin: 10px -13px;
        text-align: left;
        font-size: 12px;
        font-weight: 500;

        .col-sm-6{
            padding-left:14px;
            padding-right:7px;

            label{
                margin-top:28px
            }
        }
        
        input , textarea{
            width:100%;
        }

        textarea{
            resize: none;
            height:210px;
        }
    }

    button{
        color: white;
        background-color: rgb(64,50,37);
        padding: 7px 40px;
    }
}

</style>