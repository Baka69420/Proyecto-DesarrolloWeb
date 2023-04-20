<template>
    <div id="title">
        <h1>Denos Feedback</h1>
    </div>
    <form>
        <div class="data">
            <label for="nombre">Nombre:</label>
            <input class="text-input" name="nombre" type="text">
        </div>
        <div class="data">
            <label for="email">Email:</label>
            <input class="text-input" name="email" type="email">
        </div>
        <div class="data">
            <label for="nacimiento">Fecha Nacimiento:</label>
            <input class="text-input" name="nacimiento" type="date">
        </div>
        <div id="radio-options" class="data">
            <label for="genero">Genero:</label>
            <div>
                <div class="radio-option">
                    <input name="genero" type="radio" value="F">
                    <label for="genero">Femenino</label>
                </div>
                <div class="radio-option">
                    <input name="genero" type="radio" value="M">
                    <label for="genero">Masculino</label>
                </div>
                <div class="radio-option">
                    <input name="genero" type="radio" value="O">
                    <label for="genero">Otro</label>
                </div>
            </div>
        </div>
        <div class="data">
            <label for="gradoAcad">Grado Academico:</label>
            <select name="gradoAcad" id="gradoAcad">
                <option value="diplomado">Primaria</option>
                <option value="secundaria">Secundaria</option>
                <option value="Universitario">Universitario</option>
            </select>
        </div>
        <div class="data">
            <label for="rating">Rating:</label>
            <select name="rating" id="gradoAcad">
                <option value="1">1 - No le gusto y no lo recomendaria</option>
                <option value="2">2 - No le gusto, pero lo recomendaria</option>
                <option value="3">3 - Le gusto, pero no es su favorito</option>
                <option value="4">4 - Le gusto bastante y lo recomendaria</option>
                <option value="5">5 - Le encanto y lo recomendaria</option>
            </select>
        </div>
        <button type="submit">Aceptar</button>
        <button type="reset">Cancelar</button>
    </form>
</template>

<style scoped>
#title {
    color: #ffa753;
    text-align: center;
    border-bottom: 2px solid #ffa753;
    margin-bottom: 20px; 
}

form .data label, form .data .text-input, form .data select {
    display: block;
    width: 80%;
    margin: 0 auto;
}

form #radio-options {
    display: flex;
    width: fit-content;
    margin: 0 auto;
    gap: 20px;
}

form #radio-options * {
    width: fit-content;
}

.radio-option {
    display: flex;
    width: fit-content;
}

.radio-option label {
    padding-left: 10px;
}

form button {
    display: block;
    background-color: #ffa753;
    border-radius: 10px;
    width: 80%;
    height: 40px;
    margin: 10px auto;
}

/* form {
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
} */
</style>