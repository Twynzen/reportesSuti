### IMPACTO Y PROBABILIDAD

### PROGRESO DE APRENDIZAJE

```ts
getLevelPachImpac() {
  this.formImpact.patchValue({
    level: this.JSONdataImpact?.level,
    scale: this.JSONdataImpact?.impactoScale[0],
    detail: this.JSONdataImpact?.impactoScale[0].detail,
    definition: this.JSONdataImpact?.impactoScale[0].definition,
    criteria: this.JSONdataImpact?.impactoScale[0].criteria,
  })
}

formImpact: FormGroup = this.fb.group({
  scale: new FormControl(null),
  detail: new FormControl(null),
  level: new FormControl(null),
  definition: new FormControl(null),
  criteria: new FormControl(null),
})
```
## Se realizó un formulario reactivo con su respectiva función, el cual se encuentra en la parte superior. El código se puede explicar de la siguiente manera:

// Definición de la función "getLevelPachImpac"
```ts
getLevelPachImpac() 
```
// Se accede al formulario de impacto y se utilizan los valores del objeto "JSONdataImpact" para asignar valores a los campos del formulario.
this.formImpact.patchValue({

kotlin
Copy code
// Se asigna el valor del nivel de impacto al campo "level" del formulario.
level: this.JSONdataImpact?.level,

// Se asigna el primer elemento de la matriz "impactoScale" al campo "scale" del formulario.
scale: this.JSONdataImpact?.impactoScale[0],

// Se asigna el valor del detalle del primer elemento de "impactoScale" al campo "detail" del formulario.
detail: this.JSONdataImpact?.impactoScale[0].detail,

// Se asigna el valor de la definición del primer elemento de "impactoScale" al campo "definition" del formulario.
definition: this.JSONdataImpact?.impactoScale[0].definition,

// Se asigna el valor de los criterios del primer elemento de "impactoScale" al campo "criteria" del formulario.
criteria: this.JSONdataImpact?.impactoScale[0].criteria,
})
}

Explicación del formulario:
// Importación de los módulos necesarios para la definición del formulario
import { FormGroup, FormControl, FormBuilder } from '@angular/forms';

// Definición del formulario "formImpact"
formImpact: FormGroup = this.fb.group({

// Definición del campo "scale" del formulario.
scale: new FormControl(null),

// Definición del campo "detail" del formulario.
detail: new FormControl(null),

// Definición del campo "level" del formulario.
level: new FormControl(null),

// Definición del campo "definition" del formulario.
definition: new FormControl(null),

// Definición del campo "criteria" del formulario.
criteria: new FormControl(null),
})

### DIFICULTADES:

- Se presentaron varias dificultades al momento de definir los objetos ya que no los definía correctamente.
- Se presentaron uno o dos problemas de lógica ya que la función "getLevelPachImpac" no estaba diseñada correctamente.
- Se logró dar solución al problema con ayuda de Daniel y se despejaron varias dudas respecto al tema de formularios reactivos. También obtuve ayuda de Chat OpenAI, la cual me proporcionó ayuda para lograr comprender qué error tenía en el código.

### PREGUNTAS Y/O COMENTARIOS:

- Me parece que el proyecto es muy interesante, ya que en él se pueden reforzar temas de Angular y TS, los cuales son fundamentales para su funcionamiento. Además, adquirimos más conocimiento y experiencia en el campo del desarrollo.

### PLAN PARA EL DÍA SIGUIENTE:

- Para el día de mañana, realizaré una adición al código en las funciones de selección de estos formularios. La intención es que cuando el usuario seleccione alguna escala, se genere un cambio en las otras partes del formulario (detail, description, criteria) a la que corresponda la escala seleccionada.
- Se utilizará el recurso de Chat OpenAI y materiales como tutoriales, entre otros.
