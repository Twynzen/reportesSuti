# IMPACTO Y PROBABILIDAD

## PROGRESO DE APRENDIZAJE

Se crearon las siguientes funciones, al principio, cuando vi este código, me resultó un poco confuso entender lo que estaba haciendo. Sin embargo, después de revisarlo cuidadosamente y experimentar con él, finalmente pude comprender su función.

```ts
onSelectImpac(event: any) {
  const selectedIndex = event.value;
  const selectedScale = this.JSONdataImpact?.impactoScale[selectedIndex];
  this.formImpact.patchValue({
    detail: selectedScale.detail,
    definition: selectedScale.definition,
    criteria: selectedScale.criteria
  });
}

onSelectProbability(event: any) {
  const selectedIndex = event.value;
  const selectedScale = this.JSONdataImpact?.probabilidadScale[selectedIndex];
  this.formProbability.patchValue({
    detail: selectedScale.detail,
    definition: selectedScale.definition,
    criteria: selectedScale.criteria
  });
}
```
Estas dos funciones se utilizan para actualizar los campos de un formulario de evaluación de riesgos en función de los niveles de impacto y probabilidad seleccionados. Al seleccionar un valor de un menú desplegable, la función toma el índice seleccionado y busca la definición correspondiente en una lista de definiciones. Luego, actualiza los campos del formulario con los detalles de esa definición.

En general, a medida que trabajé con este código, pude ver un progreso en mi aprendizaje y habilidades de programación. Aprendí cómo trabajar con menús desplegables, cómo buscar y actualizar valores en una lista de definiciones y cómo utilizar estas habilidades en el contexto de una aplicación de evaluación de riesgos. 

## DIFICULTADES

 Al principio en este codigo me parecio  difícil entender la sintaxis, especialmente si soy nuevo en la programación.Poco a poco fui entendiendo la manera que funcionaba el y como se relacionaba cada funcion, despues de realizarla no queria funcionar, se verifico varias veces, con ayuda de Daniel pude resolver mis dudas  y detectar el error, ya que se presentaba en una letra en el formulario HTML.  

## PREGUNTAS Y/O COMENTARIOS

Pienso que el proyecto es una muy buena forma de aprender ya que me permite modificarlo y verificar si funcionamiento, tambien esta diseñado de una manera que sea relativamente facil de comprtender.

Me gustaria mas aprender de Angular y ts, a veces se me dificulta saber o interpretar las variables, me gustaria aprender mas como definirlas en el proyecto y tambien comprender mejor su funcionalidad.

Deseo aprender mas sobre Formularios Reactivos

## PLAN PARA EL DIA DE MAÑANA:

Mi objetivo es reforzar lo aprendido en el transcurso de la semana, deseo aprender mucho mas e implementarlo de una manera eficiente en el proyecto y en los demas proyectos que tiene la compañia, para mañana investigare como guardar datos que ingrese el cliente en el formulario reactivo.
