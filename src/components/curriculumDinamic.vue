<template>
    <div class="containerTitulo">
        <span class="titulo">Personaliza el CV con tus datos</span>
    </div>
    <div class="contenedorPrincipal">

        <!-- Estructura del formulario para llenar datos -->

        <div class="containerForm">
            <label>Nombre</label>
            <input type="text" v-model="nombre" placeholder="Ej: Amaia Uribe Mendoza">
            <label>Especialidad</label>
            <input type="text" v-model="especialidad" placeholder="Ej: Desarrollador Web">
            <label>Nombre de la empresa de tu último trabajo y el tiempo que laboraste</label>
            <input type="text" v-model="empresa1" placeholder="Ej: Mi empresa Sep 2019 - actualidad">
            <label>Nombre del puesto que tenías en tu último trabajo</label>
            <input type="text" v-model="puesto1" placeholder="Ej: Gerente general">
            <label>Descripción breve de tus funcionalidades en tu puesto</label>
            <input type="text" v-model="descripcion1">
            <label>Nombre de la empresa de tu penúltimo trabajo y el tiempo que laboraste</label>
            <input type="text" v-model="empresa2" placeholder="Ej: Mi empresa 2015 - 2016">
            <label>Nombre del puesto que tenías en tu penúltimo trabajo</label>
            <input type="text" v-model="puesto2" placeholder="Ej: Ayudante de contabilidad">
            <label>Descripción breve de tus funcionalidades en tu puesto</label>
            <input type="text" v-model="descripcion2">
            <label>Menciona trabajos por tu cuenta o cursos que estes realizando en este momento</label>
            <input type="text" v-model="otros1" placeholder="Ej: Curso de ingles en Mi escuela">
            <input type="text" v-model="otros2" placeholder="Ej: Certificado en Marketing por Google">
            <label>Breve descripción de quien eres, tus pasiones, aptitudes, etc.</label>
            <input type="text" v-model="sobreMi">
            <label>Escribe tu educación</label>
            <input type="text" v-model="educacion1"
                placeholder="Ej: 2023 -Ingeniería en sistemas computacionales. UTEL universidad.">
            <input type="text" v-model="educacion2" placeholder="Ej: 2022 - Programadora Full Stack. Generation México.">
            <input type="text" v-model="educacion3"
                placeholder="Ej: 2018 - Técnica en Administración de Recursos Humanos. CETis 154.">
            <label>Teléfono</label>
            <input type="text" v-model="telefono" placeholder="Ej: 55 2045 7713">
            <label>Correo electrónico</label>
            <input type="text" v-model="correo" placeholder="Ej: amaia@gmail.com">
            <label>Recidencia</label>
            <input type="text" v-model="recidencia" placeholder="Ej: Monterrey, México">
        </div>

        <!-- Estructura del CV dinamico -->

        <div class="container1">
            <div class="hoja">
                <div class="containerLeft">
                    <img class="fotoPerfil" src="@/../public/FotoPerfil.jpeg" alt="Foto de perfil">
                    <h2>SOBRE MÍ</h2>
                    <P class="sobreMi">{{ sobreMi }}</P>
                    <h2>EDUCACIÓN</h2>
                    <p class="educacion">{{ educacion1 }}</p>
                    <p class="educacion">{{ educacion2 }}</p>
                    <p class="educacion">{{ educacion3 }}</p>
                    <h2>DATOS DE <br />CONTACTO</h2>
                    <div class="containerIconos">
                        <img class="iconos" src="@/../public/telefono.png" alt="icono representativo de un teléfono">
                        <span class="contacto">{{ telefono }}</span>
                    </div>
                    <div class="containerIconos">
                        <img class="iconos" src="@/../public/correo.png" alt="icono representativo del correo electrónico">
                        <span class="contacto">{{ correo }}</span>
                    </div>
                    <div class="containerIconos">
                        <img class="iconos" src="@/../public/localizador.png" alt="icono representativo de localización">
                        <span class="contacto">{{ recidencia }}</span>
                    </div>
                </div>
                <div class="containerRight">
                    <h1>{{ nombre }}</h1>
                    <h2 class="especialidad">{{ especialidad }}</h2>
                    <H2 class="experiencia">EXPERIENCIA LABORAL</H2>
                    <div class="descripciones">
                    <H3>{{ empresa1 }}</H3>
                    <b>{{ puesto1 }}</b>
                    <p class="descripcion">{{ descripcion1 }}</p>
                    <H3>{{ empresa2 }}</H3>
                    <b>{{ puesto2 }}</b>
                    <p class="descripcion">{{ descripcion2 }}</p>
                </div>
                    <H2>OTROS</H2>
                    <ul>
                        <li class="list">{{ otros1 }}</li>
                        <li class="list">{{ otros2 }}</li>
                    </ul>
                </div>
            </div>
        </div>
    </div>

    <!-- Botón para descargar PDF -->
    <div class="conatinerBoton">
        <button class="boton" @click="generarPDF">Descargar CV</button>
    </div>
</template>

<script>
import pdfMake from "pdfmake/build/pdfmake";
import pdfFonts from "pdfmake/build/vfs_fonts";

pdfMake.vfs = pdfFonts.pdfMake.vfs;

export default {
    name: 'curriculum-dinamic',
    data() {
        return {
            nombre: '',
            especialidad: '',
            empresa1: '',
            puesto1: '',
            descripcion1: '',
            empresa2: '',
            puesto2: '',
            descripcion2: '',
            otros1: '',
            otros2: '',
            sobreMi: '',
            educacion1: '',
            educacion2: '',
            educacion3: '',
            telefono: '',
            correo: '',
            recidencia: '',
        };
    },

    /* Funcionalidad para descargar PDF */
    
    methods: {
        generarPDF() {
            const docDefinition = {
                content: [
                    { text: `${this.nombre}` },
                    { text: `${this.especialidad}` },
                    { text: `${this.empresa1}` },
                    { text: `${this.puesto1}` },
                    { text: `${this.descripcion1}` },
                    { text: `${this.empresa2}` },
                    { text: `${this.puesto2}` },
                    { text: `${this.descripcion2}` },
                    { text: `${this.otros1}` },
                    { text: `${this.otros2}` },
                    { text: `${this.sobreMi}` },
                    { text: `${this.educacion1}` },
                    { text: `${this.educacion2}` },
                    { text: `${this.educacion3}` },
                    { text: `${this.telefono}` },
                    { text: `${this.correo}` },
                    { text: `${this.recidencia}` },
                ]
            };

            pdfMake.createPdf(docDefinition).download("Curriculum");
        }
    }
};
</script>

<style>
.contenedorPrincipal {
    columns: 2;
}

.containerTitulo {
    text-align: center;
    margin-top: 50px;
    margin-bottom: 50px;
}

.titulo {
    font-family: 'Montserrat', sans-serif;
    font-size: 26px;
    font-weight: bold;

}

.containerForm {
    display: flex;
    flex-direction: column;
    width: 500px;
    margin-left: 100px;
    margin-bottom: 50px;
}

label {
    font-family: 'Montserrat', sans-serif;
    font-size: 14px;
    font-weight: bold;
    margin-bottom: 10px;
    margin-top: 10px;
    margin-left: 20px;
}

input {
    font-family: 'Montserrat', sans-serif;
    border-radius: 10px;
    height: 25px;
    border: 2px solid;
    border-color: #FFDAD3;
    padding-left: 20px;
    font-weight: bold;
    margin-bottom: 10px;

}

::placeholder {
    font-family: 'Montserrat', sans-serif;
    padding-left: 10px;
}

.conatinerBoton {
    text-align: right;
    margin-right: 350px;
    margin-bottom: 100px;
}

.boton {
    font-family: 'Montserrat', sans-serif;
    font-weight: bold;
    background-color: darksalmon;
    padding-left: 30px;
    padding-top: 10px;
    padding-right: 30px;
    padding-bottom: 10px;
    border-radius: 10px;
    border: 0;
}
.boton:hover{
    background-color: rgb(255, 218, 211, 2);
    color: darksalmon;
}
.descripciones{
    width: 270px;
    height: auto;
}

</style>