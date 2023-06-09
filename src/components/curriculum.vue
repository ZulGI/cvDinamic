<template>
    <div class="container">
        <div class="hoja">

            <!-- Estructura del contenedor izquierdo -->

            <div class="containerLeft">
                <img class="fotoPerfil" src="@/../public/FotoPerfil.jpeg" alt="Foto de perfil">
                <h2>SOBRE MÍ</h2>
                <P class="sobreMi">Soy una chica que siempre busca
                    superarse y aprender, me gusta la
                    creatividad y la lógica, soy
                    organizada, puntual, cumplida, sé
                    trabajar en equipo y siempre doy
                    lo mejor de mi en todo lo que
                    hago.
                </P>
                <h2>EDUCACIÓN</h2>
                <p class="educacion">2023 -Ingeniería en sistemas
                    computacionales. UTEL
                    universidad.
                </p>
                <p class="educacion">
                    2022- Programadora Full Stack.
                    Generation México.
                </p>
                <p class="educacion">
                    2018 - Técnica en
                    Administración de Recursos
                    Humanos. CETis 154
                </p>
                <h2>DATOS DE <br />CONTACTO</h2>
                <div class="containerIconos">
                    <img class="iconos" src="@/../public/telefono.png" alt="icono representativo de un teléfono">
                    <span class="contacto">
                        55 8496 5910
                    </span>
                </div>
                <div class="containerIconos">
                    <img class="iconos" src="@/../public/correo.png" alt="icono representativo del correo electrónico">
                    <span class="contacto">
                        sahiangarciaislas@gmail.com
                    </span>
                </div>
                <div class="containerIconos">
                    <img class="iconos" src="@/../public/localizador.png" alt="icono representativo de localización">
                    <span class="contacto">
                        Ciudad de México, México.
                    </span>
                </div>
            </div>

            <!-- Estructura del contenedor derecho -->

            <div class="containerRight">
                <h1>SAHIAN GARCÍA ISLAS</h1>
                <h2 class="especialidad">PROGRAMADORA FRONT-END</h2>
                <H2 class="experiencia">EXPERIENCIA LABORAL</H2>
                <H3>IOS COMUNICACIONES 2022 - ACTUALIDAD</H3>
                <b>Líder de programación jr</b>
                <p class="descripcion">
                    Participé en el desarrollo de una App móvil y web
                    para el trabajo de los técnicos de Totalpay, con
                    técnologías como Vue.js, Tailwind CSS, Firebase,
                    React Native, etc.
                    De igual manera realice páginas web para clientes
                    externos con WordPress y Elementor; rabajando en
                    equipo dentro de mi departamento con Marketing y
                    Diseño.

                </p>
                <H3>JUL 2022 - OGOSTO 2022</H3>
                <b>Proyecto estilo Freelance</b>
                <p class="descripcion">
                    Desarrollo de un Ecommerce para la carpintería
                    Ramaka aplicando tecnologías Front-end y Back-end
                    con lenguajes de programación como JavaScript y
                    Java, al igual que tecnologías como HTML, CSS, Figma,
                    GitBash, GitHub MySQL, entre otros. Igualmente
                    aplicando la metodología SCRUM como organización
                    de mi equipo de desarrollo
                </p>
                <H2>OTROS</H2>
                <ul>
                    <li class="list">Curso de inglés en la Universidad de Cambridge(en proceso)</li>
                    <li class="list">Curso de Google ADS en Google (en proceso)</li>
                </ul>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'cv-dinamic',
};
</script>

<style>

/* Generales */

.container {
    padding-top: 30px;
    padding-bottom: 30px;
    margin: 0;
}

.hoja {
    display: flex;
    justify-content: center;
    width: 100%;
    height: 670px;
}

/* Contenedor izquierdo */

.containerLeft {
    background-color: #FFDAD3;
    width: 160px;
    padding-left: 30px;
    padding-right: 25px;
    box-shadow: 5px 5px 90px 5px gray;

}

.fotoPerfil {
    width: 200px;
    height: 220px;
    object-fit: cover;
    margin-top: 28px;
    position: relative;
}

.sobreMi {
    font-family: 'Montserrat', sans-serif;
    font-size: 8px;
    font-weight: bold;
    text-align: justify;
    line-height: 13px;
    margin-bottom: 10px;
}

.educacion {
    font-family: 'Montserrat', sans-serif;
    font-size: 9px;
    font-weight: bold;
    margin-top: 5px;
}

.containerIconos {
    columns: 2;
    width: 500px;
    margin-bottom: 5px;
}

.contacto {
    font-family: 'Questrial', sans-serif;
    font-size: 11px;
    width: 100px;
    margin-left: 5px;
    padding-bottom: 20px;
    font-weight: 700px;
}

.iconos {
    width: 15px;
}

/* Contenedor derecho */

.containerRight {
    background-color: white;
    width: 260px;
    padding-left: 30px;
    padding-right: 30px;
}

h1 {
    font-family: 'Montserrat', sans-serif;
    margin-left: 25px;
    margin-top: 50px;
    margin-right: 10px;
    line-height: 45px;
    text-transform: uppercase;
}

.especialidad {
    font-family: 'Montserrat', sans-serif;
    font-size: 14px;
    font-style: italic;
    font-weight: bold;
    margin-left: 25px;
    text-transform: uppercase;

}

.experiencia {
    font-family: 'Montserrat', sans-serif;
    font-weight: 600;
    font-size: 14px;
    margin-top: 80px;
}

h3 {
    font-family: 'Montserrat', sans-serif;
    font-size: 11px;
    margin-top: 15px;
    margin-bottom: 2px;
    text-transform: uppercase;
}

h2 {
    font-family: 'Montserrat', sans-serif;
    font-size: 12.9px;
    text-transform: uppercase;
}

b {
    font-size: 11.4px;
}

.descripcion {
    font-family: 'Montserrat', sans-serif;
    font-size: 10.4px;
    margin-top: 3px;
}

ul {
    padding-left: 30px;
}

.list {
    font-family: 'Montserrat', sans-serif;
    font-size: 9.9px;
}</style>