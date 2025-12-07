<script setup>
import Register from './Register.vue';
import Login from './Login.vue';
import {ref} from 'vue';

const ShowLogin = ref(false);
const ShowRegister = ref(false);

</script>


<template>


    <div class="container">
        <button class="login" @click="ShowLogin = true">Iniciar Sesión</button>
        <button class="registrar" @click="ShowRegister = true">Registrate</button>

          <Login 
        :mostrarLogin ="ShowLogin"
        @cerrarLogin ="ShowLogin = false"
        />

        <Register :mostrarRegister = "ShowRegister" @cerrarRegister = "ShowRegister = false" />

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