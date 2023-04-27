### Impacto y Probabilidad

### Descripción de Actividades

Se realizó una nueva función `getLevelPach()` que es definida en un archivo de código fuente de JavaScript o TypeScript y que se utiliza para actualizar un formulario Reactivo con datos específicos. La función toma los valores de "nivel" y "escala" de un objeto JSON denominado "JSONdataImpact" y los asigna a los campos correspondientes en el formulario Reactivo.

Esta función es útil para actualizar automáticamente los valores de un formulario Reactivo con los datos de un objeto JSON específico, lo que ahorra tiempo y reduce errores al momento de ingresar los datos manualmente.

```typescript
getLevelPach() {
  this.formReactive.patchValue({
    level: this.JSONdataImpact?.level,
    scale: this.JSONdataImpact?.probabilidadScale[0]
  })
}

 <input readonly type="number" formControlName="level" />
```

### Progreso de aprendizaje: 

* En primer lugar en la creacion de un formulario Reactivo utilizando las herramientas y componentes proporcionados por el framework de desarrollo en el que se está trabajando. El formulario Reactivo es una herramienta que permite crear formularios dinámicos y con validación de datos en aplicaciones web.

## Asignación de los datos al formulario Reactivo: La función "getLevelPach()" utiliza el método "patchValue()" del objeto "formReactive" para asignar los valores de "nivel" y "escala" al formulario Reactivo. El método "patchValue()" es utilizado para actualizar los valores de los campos de un formulario Reactivo de manera programática, utilizando los datos obtenidos desde el objeto JSON.

## Actualización automática del formulario Reactivo: La función "getLevelPach()" es invocada cada vez que se requiere actualizar el formulario Reactivo con los datos obtenidos desde el objeto JSON. Esto permite que el formulario Reactivo se actualice automáticamente cada vez que los datos en el objeto JSON son modificados o actualizados.

## He utilizado diversas herramientas y tutoriales en línea para aprender y mejorar mis habilidades en Angular. He consultado tutoriales en plataformas como YouTube así como páginas web especializadas en como su pagina oficial. Estos recursos en línea me han sido de gran ayuda para adquirir nuevos conocimientos y aplicarlos en este proyecto.

## Links de referencia: https://www.google.com/search?q=formularios+reactivos&oq=&aqs=chrome.0.69i59j69i57j0i512j0i433i512j0i512l6.3091j0j15&sourceid=chrome&ie=UTF-8#fpstate=ive&vld=cid:f81b7ccd,vid:epSVNMtG80I

## https://angular.io/api/forms/ReactiveFormsModule#description
 
### Dificultades encontradas:

##  No sabia a ciencia cierta como crear bien la funcion, busque tutoriales y ayudas como chat openia y tutoriales, re4cibi ayuda de Daniel, La persona que me esta capacitando para resolver dudas que tenia, tambien me explica el codigo de una manera que sea mucho mas entendible para mi

```typescript
getLevelPach() {
  this.formReactive.patchValue({
    level: this.JSONdataImpact?.level,
    scale: this.JSONdataImpact?.probabilidadScale[0]
  })
}

```