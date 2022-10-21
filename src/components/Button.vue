<template>
    <button @click="$emit('criarburguer')" class="submit-btn"  value="Criar meu Burguer">Criar meu Burguer</button>    
</template>

<script>
export default {
    
}
</script>

<style scoped>
.submit-btn{
        background-color: #222;
        color: #FCBA03;
        font-weight: bolder;
        border: 2px solid #222; 
        padding: 10px;
        font-size: 16px;
        margin: 0 auto;
        cursor: pointer;
        transition: 0.5s;
    }
    .submit-btn:hover{
        background-color: transparent;
        color: #222;
    }
    @media only screen and (min-width:2560px){
            .submit-btn{
            background-color: #222;
            color: #FCBA03;
            font-weight: bolder;
            border: 2px solid #222; 
            padding: 10px 15px;
            font-size: 40px;
            margin: 0 auto;
            cursor: pointer;
            transition: 0.5s;
            width: 400px;
            height: 140px;
            border-radius: 3%;
        
        }
    }
</style>