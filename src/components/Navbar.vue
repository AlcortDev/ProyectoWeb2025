<script setup>
import LoginMenu from './LoginMenu.vue';
</script>

<template>
<div class="navbar">
    <div class="logo">
        Talleres.com
    </div>
    <div class= "menu">
        <button class="menu_button">Inicio</button>
        <button class="menu_button">Nosotros</button>
        <button class="menu_button">Contacto</button>
        <button class="menu_button">Preguntas Frecuentes</button>
    </div>

    <div class="login-menu">
        <LoginMenu/>
    </div>
</div>

</template> 

<style scoped>
.navbar{
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    align-items: center;
    height: 50px;
    width: 100%;
    background-color: rgb(202, 0, 0);
    position:fixed; 
    box-shadow: 0px 4px 5px 5px rgba(0, 0, 0,0.3);
    padding: 0px 20px;

}

.menu,.login-menu{
    display: flex;
    flex-direction: row; 
    gap: 5px;
    height: inherit;
}




button{
    text-decoration: none;
    
}
</style>

