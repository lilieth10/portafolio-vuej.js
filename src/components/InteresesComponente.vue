<script setup>
import { ref } from 'vue';
import FondoLava from './FondoLava.vue';
//Este es un arreglo con ref para que se pueda reactivar el cambio de los intereses
const intereses = ref([
    'Desarrollo de Software de Código Abierto: Me gusta contribuir a proyectos en GitHub, y colaborar con otros devs que me permita tanto enseñar lo que se como aprender de ellos...',
    'Deportes al Aire Libre: Disfruto de la naturaleza y caminar para mantener un equilibrio entre el trabajo y la vida personal.',
    'Tecnología de Innovación: Me apasiona explorar nuevas tendencias tecnológicas como la inteligencia artificial y el desarrollo de aplicaciones móviles.',
    'Baile: Practico el baile como un hobby, disfruto y me siento bien conmigo mima al bailar.'
]);
</script>

<template>
    <div class="intereses-contenedor">
        <FondoLava />
        <ul class="contenedor-lista">
            <li class="item" v-for="interes in intereses" :key="interes">
                {{ interes }}
            </li>
        </ul>
    </div>
    <!-- <div class="intereses-contenedor">
        <ul class="contenedor-lista">
            <li class="item">
                Desarrollo de Software de Código Abierto: Contribuyo a proyectos en GitHub, colaborando con otros
                desarrolladores para mejorar herramientas y librerías populares.
            </li>
            <li class="item">
                Deportes al Aire Libre: Disfruto del senderismo y el ciclismo de montaña, actividades que practico
                regularmente para mantener un equilibrio entre el trabajo y la vida personal.
            </li>
            <li class="item">
                Tecnología de Innovación: Me apasiona explorar nuevas tendencias tecnológicas como la inteligencia
                artificial y el desarrollo de aplicaciones móviles.
            </li>
            <li class="item">
                Fotografía: Practico la fotografía como un hobby, lo que me ayuda a mantener una perspectiva creativa
                tanto en mi vida profesional como personal.
            </li>
        </ul>
    </div> -->
</template>

<style scoped>
.intereses-contenedor {  
    display: flex;  
    position: relative;  
    margin: 0 auto;  
    max-width: 85%;  
    padding: 1rem;  
    background: linear-gradient(135deg, rgba(255, 105, 180, 1) 0%, rgba(138, 43, 226, 1) 100%); /* Gradiente de rosa a lila */  
    border-radius: 8px; /* Opcional: para redondear las esquinas */  
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2); /* Opcional: sombra para dar profundidad */  
}  

.contenedor-lista {  
    list-style-type: none;  
    padding: 1rem;  
    margin-bottom: .5rem;  
    color: var(--vt-c-white-soft); /* O puedes usar un color blanco puro aquí si corresponde */  
    font-size: 1.4rem;  
    text-shadow: 3px 3px 6px rgba(0, 0, 0, 1);  
}  

.item {  
    margin-bottom: 1rem;  
    padding: 8px; /* Espaciado interno para los elementos de la lista */  
    background: rgba(255, 255, 255, 0.1); /* Fondo ligeramente transparente para los items */  
    border-radius: 5px; /* Opcional: redondear las esquinas para los items */  
}
</style>