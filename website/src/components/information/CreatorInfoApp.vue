<template>
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
#creator-info {
    margin: 0 auto;
    height: 125px;
    width: fit-content;
    display: flex;
    align-items: center;
    gap: 10px;
}

#profile-pic {
    height: 100%;
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
</style>