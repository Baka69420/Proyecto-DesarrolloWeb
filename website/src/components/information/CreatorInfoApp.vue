<template>
    <div id="title">
        <h1>Creador de la pagina web</h1>
    </div>
    <div id="creator-info">
        <div id="profile-pic">
            <img src="@/assets/images/creator-pic.png" alt="Picture of the Creator">
        </div>
        <div id="course-info">
            <p><strong>Estudiante:</strong> Rafael Eduardo Alvarado Zuñiga</p>
            <p><strong>Cedula:</strong> 2-0833-0156</p>
            <p><strong>Curso:</strong> Diseño de Aplicaciones Web (ISW-512)</p>
            <p><strong>Profesor:</strong> Rafael Eduardo Alvarado Zuñiga</p>
        </div>
    </div>
</template>

<style scoped>
#title {
    color: #ffa753;
    text-align: center;
    border-bottom: 2px solid #ffa753;
    margin-bottom: 20px; 
}

#creator-info {
    margin: 0 auto;
    width: fit-content;
    display: flex;
    align-items: center;
    gap: 10px;
}

#profile-pic {
    height: 125px;
    border-radius: 5px;
    border: double black 2px;
    overflow: hidden;
}

#profile-pic img {
    height: 100%;
}

#course-info p {
    margin: 5px;
}

@media only screen and (max-width: 575px) {
  #creator-info {
    flex-direction: column;
  }
}

@media only screen and (min-width: 575px) {
    #creator-info {
      flex-direction: row;
    }
}
</style>