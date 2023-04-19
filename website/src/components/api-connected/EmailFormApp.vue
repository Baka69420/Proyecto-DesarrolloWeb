<template>
    <div id="title">
        <h1>Formulario de Contacto por Email</h1>
    </div>
    <form>
        <div id="name">
            <label for="Nombre">Nombre:</label>
            <input type="text">
        </div>
        <div id="email">
            <label for="Email">Email:</label>
            <input type="email">
        </div>
        <div id="subject">
            <label for="Asunto">Asunto:</label>
            <input type="text">
        </div>
        <div id="message">
            <label for="Mensaje">Mensaje:</label>
            <input type="text">
        </div>
        <div id="buttons">
            <button type="submit">Enviar</button>
            <button type="reset">Cancelar</button>
        </div>
    </form>
</template>

<style scoped>
#title {
    color: #ffa753;
    text-align: center;
    border-bottom: 2px solid #ffa753;
    margin-bottom: 20px; 
}

form {
    width: fit-content;
    display: flex;
    flex-direction: column;
    gap: 5px;
    margin: 0 auto;
}

form * {
    margin-left: auto;
    display: flex;
    flex-direction: row;
    gap: 5px;
}

form #buttons {
    width: 100%;
}

form #buttons button {
    background-color: #ffa753;
    border-radius: 10px;
    width: 50%;
    height: 40px;
}
</style>