# IMPACTO Y PROBABILIDAD

## PROGRESO DE APRENDIZAJE

## Intervalo y Referencia

Hoy se adicionó una nueva funcionalidad a la página web, que permite al usuario ver la cantidad de retiros (débitos) y consignaciones (créditos) en una cuenta bancaria. Para ello, se agregaron dos tarjetas que muestran la información correspondiente en la página principal.

Para implementar esta funcionalidad, se agregó el siguiente código en la página web:

``` ts
<div class="card-content">
    <label for="">Cantidad de Retiros (débitos)</label>
    <div class="card-form">
        <select (change)="onSelect6Change($event.target)">
            <ng-container>
                <option
                    *ngFor="let scala of JSONdataImpactTrans.montoRetirosScale; let p = index"
                    [value]="p">
                    {{scala.name}}
                </option>
            </ng-container>
        </select>
        <div class="container-crit-def-min">
            <div>
                <label for="">Media:</label>
                <input type="text" placeholder="Ingresar"
                    [(ngModel)]="JSONdataImpactTrans.montoRetirosScale[detail6].media">
            </div>
            <div>
                <label for="">Desviación:</label>
                <input type="text" placeholder="Ingresar"
                    [(ngModel)]="JSONdataImpactTrans.montoRetirosScale[detail6].desviacion">
            </div>
            <div>
                <label for="">Mínimo:</label>
                <input type="text" placeholder="Ingresar"
                    [(ngModel)]="JSONdataImpactTrans.montoRetirosScale[detail6].minimo">
            </div>
            <div>
                <label for="">Máximo:</label>
                <input type="text" placeholder="Ingresar"
                    [(ngModel)]="JSONdataImpactTrans.montoRetirosScale[detail6].maximo">
            </div>
        </div>
        <div class="detail">
            <input type="text"
                [(ngModel)]="JSONdataImpactTrans.montoRetirosScale[detail6].detail"
                (ngModelChange)="inputValueChange($event)">
        </div>
    </div>
</div>

```

Cada tarjeta contiene un menú desplegable que permite al usuario seleccionar una escala de visualización. Los valores correspondientes se muestran en cuatro campos de entrada: media, desviación, mínimo y máximo. Además, hay un campo de entrada adicional para proporcionar información detallada sobre la escala seleccionada.

Adicionalemte se realizo una documentacion de como funciona este codigo en el HTML.

## DIFICULTADES

Estoy teniendo algunas dificultades al escribir el código para las nuevas secciones de la página web. Como principiante, me resulta un poco difícil comprender algunos de los elementos de HTML que estoy utilizando, así como vincular los campos de entrada a los valores correspondientes de la escala seleccionada en el menú desplegable. Pero con ayuda de Daniel y chat openai he logrado resolver varias dudas sobre el correcto desarrollo de las secciones.

## PREGUNTAS Y/O COMENTARIOS

Enfocare mis esfuerzos en aprender cómo utilizar funciones en JavaScript y cómo estas se relacionan con los elementos HTML para llevar a cabo acciones específicas. Entender los fundamentos de la programación y los conceptos de la lógica detrás de las funciones sería crucial para comprender el trabajo realizado, tambien hacer mejoras en el futuro.

## PLAN PARA EL DIA DE MAÑANA

Para el dia de mañana se revisara este codigo con ayuda de Daniel, adicional se verificara el TS de Impacto y Probabilidad.