<script setup>
import Login from './Login.vue';
import {ref} from 'vue';

const ShowLogin = ref(false);

</script>


<template>


    <div class="container">
        <button class="login" @click="ShowLogin = true">Iniciar Sesión</button>
        <button class="registrar">Registrate</button>

          <Login 
        :mostrar ="ShowLogin"
        @cerrar ="ShowLogin = false"
        />


    </div>

    
  
</template>

<style scoped>
.container{
    
    display: flex;
    

}

button{
    
    width: inherit;
    color: var(--color-fondo);
    padding: 0 15px;
    &:hover{
        background-color: var(--color-acento);
        cursor: pointer;
    }
}


</style>