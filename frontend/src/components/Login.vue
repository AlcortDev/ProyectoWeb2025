<script setup>

defineProps({
    mostrarLogin: Boolean
})

</script>

<template>
    <div class="overlay "  v-show="mostrarLogin">
        <div class ="login_container" >

            <button class="btn_close" @click="$emit('cerrarLogin')">X</button>
            <div class="logo">Talleres.com</div>
            <form action="" class="formulario">

                <label for="UsrEmail" id="labelUsrEmail">Correo eléctronico</label>
                <input type="text" id="UsrEmail" name="UsrEmail" placeholder="Ingresa tú correo eléctronico" >

                <label for="UsrPass" id="labelUsrPass"> Contraseña:</label>
                <input type="password" id="UsrPass" name="UsrPass" placeholder="Ingresa tu contraseña">

                <input type="submit" value="Iniciar Sesión" id="SubmitBtn">

                
            </form>
        </div>
    </div>
</template>

<style scoped>

@import url(src/assets/main.css);





.overlay{
        display: flex;
        justify-content: center;
        align-items: center;

        position:fixed;

        inset: 0 !important;
        z-index: 100;
        top: 0;
        left: 0;
        margin:0;
        padding: 0;
        height: 100%;
        width: 100%;
        background-color: rgba(0,0,0,0.3);
    }

.login_container{
        background-color:var(--color-fondo);
        width: 400px;
        max-width: 700px;
        height: 80vh;
        padding: 2rem 2rem;
        border-radius: 10px;
        position:relative;
        display: flex;
        flex-direction: column;
        justify-content: space-around;
    }

.logo{
    display:inherit;
    justify-content: center;
    align-items: center;

    background-color: var(--color-acento);
    color: var(--color-fondo);
    font-weight: bolder;
    text-align: center;
    border-radius:6px;
    height: 50px;
    width: wrap;
    padding: 10px 30px;
    
}

    

.btn_close{
        color:black;
        background-color: #c5c5c5;
        padding:13px 16px;
        border-radius: 50%;
        position: absolute;
        right:5px;
        top: 5px;
        
        font-size: 1rem;

        transition:all 0.3s ease;

        &:hover{
            background-color: #797777;   
            cursor:pointer; 
        }
    }

.formulario{
        display: inherit;
        flex-direction: column;
        gap: 1rem;
        width: 100%;
    }

#labelUsrEmail, #labelUsrPass{
    font-family: "Roboto", Arial, Helvetica, sans-serif;
    font-weight: bold;

}

#UsrEmail, #UsrPass{
    width: 100%;
    border: 1px solid var(--color-acento) ;
    padding: 5px 15px ;
    border-radius: 6px;
    transition: all 0.1s ease;

    &:focus{
        outline:none;
        border: 2px solid var(--color-primario);
        padding:10px 15px;

    }
}

#SubmitBtn{
    color: var(--color-fondo);

    margin: 0 auto;
    text-align: center;
    width: 60%;
    padding: 6px 0px;
    background-image: linear-gradient(90deg, var(--color-primario), var(--color-acento));
    border: none;
    border-radius: 6px;
    transition: all 300ms ease-in-out;


    &:hover{
        scale: 1.1;
        background-image: linear-gradient(45deg, var(--color-primario), var(--color-acento));
        cursor:pointer;

    }

}


</style>

