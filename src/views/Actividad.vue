<template lang="pug">
  .curso-main-container.pb-3
    BannerInterno(icono="far fa-question-circle" titulo="Actividad didáctica")
    .container.tarjeta.tarjeta--blanca.p-4.p-md-5
  
      #Actividad                
        <Actividad :cuestionario="cuestionario"/>
  
  </template>

<script>
import Actividad from 'ecored-pkg-fliz/plugin/components/actividad/Actividad.vue'
export default {
  name: 'ActividadDidactica',
  components: {
    Actividad,
  },
  data: () => ({
    cuestionario: {
      tema: 'Microcontroladores y sensores',
      titulo: 'Cuestionario',
      introduccion:
        '<b> Objetivo:</b> Evaluar la comprensión y el uso adecuado de las herramientas básicas en la ventana <em>Board</em> del <em>software</em> EAGLE.',
      barajarPreguntas: true,
      titulo_aprobado: '¡BUEN TRABAJO!',
      titulo_reprobado: 'VUELVA A INTENTARLO',
      preguntas: [
        {
          id: 1,
          texto:
            '¿Qué componente es fundamental en la construcción del molde de calzado Oxford?',
          imagen: require('@/assets/actividad/imagen1.png'),
          barajarRespuestas: true,
          opciones: [
            { id: 'a', texto: 'Puntos y líneas.', esCorrecta: false },
            { id: 'b', texto: 'Puntos y líneas guía.', esCorrecta: true },
            { id: 'c', texto: 'Tipo de cuero.', esCorrecta: false },
            { id: 'd', texto: 'Cantidad de cordones.', esCorrecta: false },
          ],
          mensaje_correcto: '¡Muy bien! Ha acertado la respuesta.',
          mensaje_incorrecto: 'Lo sentimos, su respuesta no es la correcta.',
        },
        {
          id: 2,
          texto:
            '¿Cómo se denomina el primer patrón que se genera a partir de la máscara compensada?',
          imagen: require('@/assets/actividad/imagen2.png'),
          barajarRespuestas: true,
          opciones: [
            { id: 'a', texto: 'Molde de forro.', esCorrecta: false },
            { id: 'b', texto: 'Molde de lengüeta.', esCorrecta: false },
            { id: 'c', texto: 'Molde patrón.', esCorrecta: true },
            { id: 'd', texto: 'Molde de talón.', esCorrecta: false },
          ],
          mensaje_correcto: '¡Muy bien! Ha acertado la respuesta.',
          mensaje_incorrecto: 'Lo sentimos, su respuesta no es la correcta.',
        },
        {
          id: 3,
          texto:
            '¿Qué variación del Oxford incorpora una puntera decorativa en forma de "W"?',
          imagen: require('@/assets/actividad/imagen3.png'),
          barajarRespuestas: true,
          opciones: [
            { id: 'a', texto: 'Oxford liso.', esCorrecta: false },
            { id: 'b', texto: 'Oxford con puntera.', esCorrecta: true },
            { id: 'c', texto: 'Oxford con talón.', esCorrecta: false },
            { id: 'd', texto: 'Oxford con bigotera.', esCorrecta: false },
          ],
          mensaje_correcto: '¡Muy bien! Ha acertado la respuesta.',
          mensaje_incorrecto: 'Lo sentimos, su respuesta no es la correcta.',
        },
        {
          id: 4,
          texto:
            '¿Qué medida se suma al número de horma para obtener la altura del talón en calzado de hombre?',
          imagen: require('@/assets/actividad/imagen4.png'),
          barajarRespuestas: true,
          opciones: [
            { id: 'a', texto: '20 mm.', esCorrecta: false },
            { id: 'b', texto: '30 mm.', esCorrecta: true },
            { id: 'c', texto: '18 mm.', esCorrecta: false },
            { id: 'd', texto: '15 mm.', esCorrecta: false },
          ],
          mensaje_correcto: '¡Muy bien! Ha acertado la respuesta.',
          mensaje_incorrecto: 'Lo sentimos, su respuesta no es la correcta.',
        },
        {
          id: 5,
          texto:
            '¿Qué pieza se construye a partir de dos partes simétricas recortadas de la máscara compensada?',
          imagen: require('@/assets/actividad/imagen1.png'),
          barajarRespuestas: true,
          opciones: [
            { id: 'a', texto: 'Molde de talón.', esCorrecta: false },
            { id: 'b', texto: 'Molde de lengüeta.', esCorrecta: false },
            { id: 'c', texto: 'Camisa (trepa).', esCorrecta: true },
            { id: 'd', texto: 'Cordonería.', esCorrecta: false },
          ],
          mensaje_correcto: '¡Muy bien! Ha acertado la respuesta.',
          mensaje_incorrecto: 'Lo sentimos, su respuesta no es la correcta.',
        },
        {
          id: 6,
          texto: '¿Qué característica define al calzado Oxford liso?',
          imagen: require('@/assets/actividad/imagen2.png'),
          barajarRespuestas: true,
          opciones: [
            {
              id: 'a',
              texto: 'Incluye brogueado decorativo.',
              esCorrecta: false,
            },
            {
              id: 'b',
              texto: 'Tiene múltiples piezas unidas por costuras visibles.',
              esCorrecta: false,
            },
            {
              id: 'c',
              texto: 'Presenta un diseño limpio y sin decoraciones.',
              esCorrecta: true,
            },
            {
              id: 'd',
              texto: 'Posee perforaciones en toda la estructura.',
              esCorrecta: false,
            },
          ],
          mensaje_correcto: '¡Muy bien! Ha acertado la respuesta.',
          mensaje_incorrecto: 'Lo sentimos, su respuesta no es la correcta.',
        },
        {
          id: 7,
          texto:
            '¿Qué material se recomienda para elaborar maquetas de comprobación en una etapa preliminar?',
          imagen: require('@/assets/actividad/imagen3.png'),
          barajarRespuestas: true,
          opciones: [
            { id: 'a', texto: 'Cuero.', esCorrecta: false },
            { id: 'b', texto: 'Telford.', esCorrecta: false },
            { id: 'c', texto: 'Cambrelle.', esCorrecta: false },
            { id: 'd', texto: 'Cartulina o papel kraft.', esCorrecta: true },
          ],
          mensaje_correcto: '¡Muy bien! Ha acertado la respuesta.',
          mensaje_incorrecto: 'Lo sentimos, su respuesta no es la correcta.',
        },
        {
          id: 8,
          texto:
            '¿En qué proceso se realiza un promedio entre las curvas de las máscaras interna y externa?',
          imagen: require('@/assets/actividad/imagen4.png'),
          barajarRespuestas: true,
          opciones: [
            { id: 'a', texto: 'Montaje del calzado.', esCorrecta: false },
            {
              id: 'b',
              texto: 'Obtención de la máscara compensada.',
              esCorrecta: true,
            },
            { id: 'c', texto: 'Dibujo de la bigotera.', esCorrecta: false },
            { id: 'd', texto: 'Ajuste de la capellada.', esCorrecta: false },
          ],
          mensaje_correcto: '¡Muy bien! Ha acertado la respuesta.',
          mensaje_incorrecto: 'Lo sentimos, su respuesta no es la correcta.',
        },
        {
          id: 9,
          texto:
            '¿Qué variación del calzado Oxford es ideal para eventos de etiqueta?',
          imagen: require('@/assets/actividad/imagen1.png'),
          barajarRespuestas: true,
          opciones: [
            { id: 'a', texto: 'Oxford con bigotera.', esCorrecta: false },
            { id: 'b', texto: 'Oxford casual.', esCorrecta: false },
            { id: 'c', texto: 'Oxford con puntera.', esCorrecta: false },
            { id: 'd', texto: 'Oxford liso.', esCorrecta: true },
          ],
          mensaje_correcto: '¡Muy bien! Ha acertado la respuesta.',
          mensaje_incorrecto: 'Lo sentimos, su respuesta no es la correcta.',
        },
        {
          id: 10,
          texto:
            '¿Qué función cumple principalmente la maqueta de comprobación?',
          imagen: require('@/assets/actividad/imagen2.png'),
          barajarRespuestas: true,
          opciones: [
            {
              id: 'a',
              texto: 'Verificar ajuste y corregir inconsistencias.',
              esCorrecta: true,
            },
            { id: 'b', texto: 'Fabricar el zapato final.', esCorrecta: false },
            {
              id: 'c',
              texto: 'Diseñar nuevos modelos de calzado.',
              esCorrecta: false,
            },
            {
              id: 'd',
              texto: 'Reducir el costo del material.',
              esCorrecta: false,
            },
          ],
          mensaje_correcto: '¡Muy bien! Ha acertado la respuesta.',
          mensaje_incorrecto: 'Lo sentimos, su respuesta no es la correcta.',
        },
        {
          id: 11,
          texto:
            'El patronaje de calzado Oxford no requiere marcar líneas guía en la horma.',
          imagen: require('@/assets/actividad/imagen3.png'),
          barajarRespuestas: true,
          opciones: [
            { id: 'a', texto: 'Falso', esCorrecta: true },
            { id: 'b', texto: 'Verdadero', esCorrecta: false },
          ],
          mensaje_correcto: '¡Muy bien! Ha acertado la respuesta.',
          mensaje_incorrecto: 'Lo sentimos, su respuesta no es la correcta.',
        },
        {
          id: 12,
          texto:
            'La línea de profundidad conecta el punto de atraque con el punto de altura del talón.',
          imagen: require('@/assets/actividad/imagen4.png'),
          barajarRespuestas: true,
          opciones: [
            { id: 'a', texto: 'Falso', esCorrecta: false },
            { id: 'b', texto: 'Verdadero', esCorrecta: true },
          ],
          mensaje_correcto: '¡Muy bien! Ha acertado la respuesta.',
          mensaje_incorrecto: 'Lo sentimos, su respuesta no es la correcta.',
        },
        {
          id: 13,
          texto:
            'La bigotera nunca debe cruzar el punto metatarsiano al ser diseñada.',
          imagen: require('@/assets/actividad/imagen1.png'),
          barajarRespuestas: true,
          opciones: [
            { id: 'a', texto: 'Falso', esCorrecta: false },
            { id: 'b', texto: 'Verdadero', esCorrecta: true },
          ],
          mensaje_correcto: '¡Muy bien! Ha acertado la respuesta.',
          mensaje_incorrecto: 'Lo sentimos, su respuesta no es la correcta.',
        },
        {
          id: 14,
          texto:
            'El molde de forro para Oxford se obtiene aplicando el mismo giro que el molde de cuero.',
          imagen: require('@/assets/actividad/imagen2.png'),
          barajarRespuestas: true,
          opciones: [
            { id: 'a', texto: 'Falso', esCorrecta: true },
            { id: 'b', texto: 'Verdadero', esCorrecta: false },
          ],
          mensaje_correcto: '¡Muy bien! Ha acertado la respuesta.',
          mensaje_incorrecto: 'Lo sentimos, su respuesta no es la correcta.',
        },
        {
          id: 15,
          texto:
            'La reseña histórica del Oxford señala su origen en Estados Unidos.',
          imagen: require('@/assets/actividad/imagen3.png'),
          barajarRespuestas: true,
          opciones: [
            { id: 'a', texto: 'Falso', esCorrecta: true },
            { id: 'b', texto: 'Verdadero', esCorrecta: false },
          ],
          mensaje_correcto: '¡Muy bien! Ha acertado la respuesta.',
          mensaje_incorrecto: 'Lo sentimos, su respuesta no es la correcta.',
        },
      ],
      mensaje_final_aprobado: '¡Excelente! Ha superado la actividad.',
      mensaje_final_reprobado:
        'Le recomendamos volver a revisar el componente formativo e intentar nuevamente la actividad didáctica.',
    },
  }),
}
</script>
