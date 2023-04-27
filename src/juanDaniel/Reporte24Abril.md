# IMPACTO Y PROBABILIDAD

## PROGRESO DE APRENDIZAJE

```ts
 saveImpactFormValues() {
    const scaleIndex = this.formImpact.get('scale')?.value;
    const detail = this.formImpact.get('detail')?.value;
    const definition = this.formImpact.get('definition')?.value;
    const criteria = this.formImpact.get('criteria')?.value;
    const num: number = parseInt(scaleIndex.name.split(" ")[1], 10);

    if (scaleIndex !== null) {
      this.JSONdataImpact.impactoScale[num -1] = {
        ...this.JSONdataImpact.impactoScale[num -1],
        detail: detail,
        definition: definition,
        criteria: criteria,
      };
    }
  }

  saveProbabilityFormValues() {

    const scaleIndex = this.formProbability.get('scale')?.value;
    const detail = this.formProbability.get('detail')?.value;
    const definition = this.formProbability.get('definition')?.value;
    const criteria = this.formProbability.get('criteria')?.value;
    const num: number = parseInt(scaleIndex.name.split(" ")[1], 10);

    if (scaleIndex !== null) {

      this.JSONdataImpact.probabilidadScale[num - 1] = {
        ...this.JSONdataImpact.probabilidadScale[num - 1],
        detail: detail,
        definition: definition,
        criteria: criteria,
      };
    } else {
      console.error('El índice de escala no es válido');
    }
  }
  ```
   Se crean los componentes `saveImpactFormValues`  y `saveProbabilityFormValues` son las funciónes que se encargan de guardar y actualizar los valores de los formularios llamados formImpact y formProbability en un objeto JSON llamado JSONdataImpact. La función extrae los valores de los campos 'scale', 'detail', 'definition' y 'criteria' de los formularios y actualiza el objeto JSONdataImpact con esta información. Específicamente, las funciónes actualizan un elemento dentro del array impactoScale y probabilidadSScale en el objeto JSONdataImpact, utilizando el valor del campo 'scale' como índice para determinar qué elemento debe ser modificado. Al actualizar el elemento, la función conserva las propiedades existentes y añade o actualiza las propiedades detail, definition y criteria con los valores extraídos del formulario.

   ```ts
1.   saveImpactFormValues() {
// Esta línea define una función llamada saveImpactFormValues que se utilizará para guardar los valores del formulario.


2.   const scaleIndex = this.formImpact.get('scale')?.value;
// Esta línea declara una constante llamada scaleIndex y asigna el valor del campo 'scale' del formulario formImpact. Si el campo 'scale' no está presente, el operador ? evitará errores y asignará undefined.


3.   const detail = this.formImpact.get('detail')?.value;
// De manera similar, esta línea declara una constante llamada detail y asigna el valor del campo 'detail' del formulario formImpact.

4.   const definition = this.formImpact.get('definition')?.value;
// Esta línea declara una constante llamada definition y asigna el valor del campo 'definition' del formulario formImpact.


5.   const criteria = this.formImpact.get('criteria')?.value;
// Esta línea declara una constante llamada criteria y asigna el valor del campo 'criteria' del formulario formImpact.


6.   const num: number = parseInt(scaleIndex.name.split(" ")[1], 10);
// Aquí, se declara una constante llamada num y se asigna el resultado de la conversión a número entero (parseInt) del segundo elemento (índice 1) del array resultante de dividir el valor de scaleIndex.name en partes separadas por espacios. El segundo argumento 10 indica que se usa la base decimal.

7.   if (scaleIndex !== null) {
// Esta línea verifica si scaleIndex no es nulo, en cuyo caso, se ejecutará el siguiente bloque de código.

8.     this.JSONdataImpact.impactoScale[num -1] = {
// Esta línea accede al elemento del array impactoScale en el objeto JSONdataImpact, utilizando num-1 como índice. Luego, se asigna un nuevo objeto al elemento seleccionado.

9.       ...this.JSONdataImpact.impactoScale[num -1],
// Esta línea utiliza el operador de propagación (spread operator) ... para copiar todas las propiedades existentes en el objeto seleccionado del array impactoScale al nuevo objeto.

10.      detail: detail,
// Esta línea asigna la constante detail al atributo detail del nuevo objeto.

11.      definition: definition,
// Esta línea asigna la constante definition al atributo definition del nuevo objeto.

12.      criteria: criteria,
// Esta línea asigna la constante criteria al atributo criteria del nuevo objeto.
```

## DIFICULTADES

Al principio en este codigo me parecio  difícil entender la sintaxis, especialmente si soy nuevo en la programación. Poco a poco fui entendiendo la manera que funcionaba el y como se relacionaba cada funcion, despues de realizarla no queria funcionar, se verifico varias veces, con ayuda de Daniel y de chat openai pude resolver mis dudas  y detectar el error, ya que no habia declarado la constante num. 

## PREGUNTAS Y/O COMENTARIOS

Este proyecto esta bien organizado y estructurado, con componentes claramente definidos y servicios modulares. Aunque soy nuevo en TypeScript, puedo ver cómo su tipado estático y características adicionales, como interfaces y clases, aportan claridad y robustez al código. Estoy emocionado de aprender más sobre cómo Angular maneja aspectos como enrutamiento, formularios y directivas, y cómo se aplican en este proyecto. Me gustaría dedicar tiempo a explorar las mejores prácticas y conceptos clave para mejorar mis habilidades de desarrollo en Angular y TypeScript.

## PLAN PARA EL DIA DE MAÑANA

Se creara y añadira la parte logica a la vista de pagiancion 


