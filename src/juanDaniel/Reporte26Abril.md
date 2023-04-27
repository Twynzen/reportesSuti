# IMPACTO Y PROBABILIDAD

## PROGRESO DE APRENDIZAJE

``` ts
saveProbabilityFormValues() {
    const actualScale = this.formProbability.get('scale')?.value;
    const actualScaleIndex = this.JSONdataImpact.probabilidadScale.findIndex((scale: { name: any; }) => scale.name === actualScale.name);
  
    if (actualScaleIndex !== -1) {
      const detail = this.formProbability.get('detail')?.value;
      const definition = this.formProbability.get('definition')?.value;
      const criteria = this.formProbability.get('criteria')?.value;
  
      this.JSONdataImpact.probabilidadScale[actualScaleIndex].detail = detail;
      this.JSONdataImpact.probabilidadScale[actualScaleIndex].definition = definition;
      this.JSONdataImpact.probabilidadScale[actualScaleIndex].criteria = criteria;
    }
  }
  findProbabilityScale(probabilityScales: any[], scaleIndex: number) {
    return probabilityScales.find(scale => scale.name === `Escala ${scaleIndex + 1}`);
  }
  ```
  Después de analizar y desarrollar el código, puedo explicar que la función se encarga de guardar los valores de un formulario de probabilidad en un objeto JSON. Primero, obtiene el valor actual de la escala del formulario y busca su índice en la estructura de datos . Si se encuentra el índice correspondiente, la función procede a obtener los valores de detalle, definición y criterio del formulario. Posteriormente, actualiza estos valores en el objeto JSON en la posición del índice encontrado. La función se utiliza para buscar una escala de probabilidad específica en un conjunto de escalas, devolviendo la escala que coincida con el índice 

``` ts
   update() {
     this.saveImpactFormValues();
     this.saveProbabilityFormValues();
    console.log(JSON.stringify(this.JSONdataImpact));
    this.impactProbabilityService
      .PostImpact(this.JSONdataImpact)
      .subscribe((data) => {
        console.log(data);
        Dialog.show('Impacto y probabilidad actualizados', Dialogtype.success);

      });
  }
```
Este código representa una función que actualiza el impacto y la probabilidad de un evento. Primero, guarda los valores en un formato especial llamado JSON. Luego, envía los datos al servidor para que se puedan guardar y actualizar. Si todo va bien, la función muestra un mensaje diciendo que los valores se han actualizado con éxito. Esto es útil porque permite mantener actualizada la información sobre un evento en particular.

## DIFICULTADES

Al principio en este codigo me parecio  difícil entender la sintaxis, especialmente porque soy nuevo en la programación. Al principio no guardaba los datos ingresados en los formularios Reactivos, luego se logro realizar que los guardata en JSONdataImpact pero surgio otro problema el cual era que no actualizaba la escala, despues de intentarlo y con ayuda de Daniel se pudo solucionar esa parte del codigo la cual me gusto aprender y a la cual  dedicare mas tiempo para aprender.

## PREGUNTAS Y/O COMENTARIOS

Me ha gustado mucho estar en este proyecto, ya que contiene muchos retos los cuales intento resolver de manera oportuna y aprendiendo un poco mas cada dia, dedicare mas tiempo a reforzar mi conocimiento en el desarrollo en Angular y TypeScript.

## PLAN PARA EL DIA DE MAÑANA

Se realizara la verificacion de codigo y se empezara a documentar la funcionalidad del mismo.
