<template>
     <!-- Esconda a MSG quando ela for vazia - OK -->
    <div v-if="teste()" id="msg-container">
        <p>{{ msg }}</p>
    </div>
</template>

<script>
    export default {
        name : "MensagemComponent",
        props :{
            msg : String
        },
        computed: {
            existeMsg(){
                return this.msg !== "" && this.msg !== null && this.msg !== undefined;
            }
        },
        methods: {
            teste(){
                if(!this.msg) {
                   return false;
                }else{
                    return true;
                }
            }
        }
    }
</script>

<style scoped>
    #msg-container {
        margin-bottom: 32px;
        padding: 16px;
        font-size: 14px;
        font-weight: bold;
        background-color: lightcyan;
        color: darkcyan;
        border-radius: 8px;
        border: dotted 3px darkcyan;
        box-shadow: 6px 6px 15px 0px gray

    }


</style>