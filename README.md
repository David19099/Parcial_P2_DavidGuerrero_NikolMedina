Programa ivernadero.

Integrantes

* Nikol Fernanda Medina Monterrey
* David Santiago Guerrero García

Descripción del proyecto
Este proyecto consiste en el desarrollo de un programa en Python para controlar el monitoreo y seguimiento automatizado de un cultivo de fresas en un invernadero equipado con sensores de temperatura y humedad relativa.
El programa solicita lecturas ambientales, valida los datos contra los rangos de los sensores, evalúa las condiciones del cultivo bajo reglas de prioridad y emite acciones correctivas o alertas.
El proceso finaliza cuando se alcanzan condiciones óptimas o de cultivo estabilizado, cuando se presenta una alerta crítica por valores fuera de rango, o cuando se completan un máximo de 8 lecturas sin estabilizarse, requiriendo revisión técnica de los equipos.
Al finalizar, el programa muestra un informe consolidado con las estadísticas y secuencias del turno.

Objetivo
Desarrollar un programa que permita:

* Registrar la temperatura y la humedad relativa del invernadero.
* Validar que los valores ingresados se encuentren dentro de los rangos válidos del sensor.
* Controlar un ciclo de repetición hasta un máximo de 8 lecturas.
* Evaluar el estado del invernadero (Óptimo, Observación o Crítico).
* Mostrar las acciones correctivas necesarias durante el estado de observación.
* Calcular los valores mínimos, máximos y promedios de temperatura y humedad.
* Almacenar y mostrar la secuencia cronológica completa de las lecturas.

Funcionamiento

1. Inicializar las constantes de rangos óptimos, críticos y válidos, así como las variables de control.
2. Solicitar la temperatura actual y la humedad actual.
3. Validar que la temperatura esté entre $[-10, 60]$ °C y la humedad entre $[0, 100]$ %.
4. Si un valor es inválido, mostrar el mensaje "Dato inválido" y volver a pedir la lectura sin contar el intento.
5. Incrementar el contador de lecturas válidas, acumular sumas, actualizar mínimos y máximos, y guardar en las listas de secuencias.
6. Verificar si se alcanzó un valor crítico (Temperatura $< 12$ o $> 32$ °C; Humedad $< 40$ o $> 90$ %).
7. Verificar si ambas variables están dentro del rango óptimo ($18 \le \text{Temperatura} \le 26$ °C y $60 \le \text{Humedad} \le 80$ %).
8. Si está en observación, determinar y mostrar las acciones correctivas (Ventilar, Calefacción, Deshumidificar o Nebulizar).
9. Controlar si se alcanzó el límite máximo de 8 lecturas.
10. Calcular los promedios finales de temperatura y humedad.
11. Mostrar el informe final consolidado del monitoreo.

Motivos de cierre / Resultados finales

* **Condiciones óptimas / Cultivo estabilizado:** Ocurre cuando ambas variables se encuentran dentro del rango óptimo.
* **Alerta crítica:** Ocurre cuando alguna variable alcanza un valor crítico, activando el protocolo de emergencia.
* **Revisión técnica de los equipos:** Ocurre cuando se completan las 8 lecturas sin que el cultivo se estabilice ni llegue a un valor crítico.

Validación de datos
El programa controla los valores inválidos y fuera de rango mediante ciclos de validación y manejo de excepciones.
Si se introduce un valor no numérico o fuera de los límites del sensor, se muestra un mensaje de error y se solicita nuevamente la lectura.

Cálculos realizados

* **Número de lecturas:** `NumeroLectura += 1`
* **Acumuladores:**
`SumaTemperaturas += TemperaturaActual`
`SumaHumedades += HumedadActual`
* **Promedios:**
`PromedioTemperatura = SumaTemperaturas / NumeroLectura`
`PromedioHumedad = SumaHumedades / NumeroLectura`

Reporte final
Al finalizar, el programa muestra:

* Resultado final y número total de lecturas tomadas.
* Temperatura mínima, máxima y promedio.
* Humedad mínima, máxima y promedio.
* Secuencia completa de temperaturas y de humedades registradas en orden cronológico.

Tecnologías utilizadas

* Python
* Programación estructurada
* Ciclos while y for
* Condicionales if-elif-else anidados
* Listas y manejo de excepciones try/except

Autores
Nikol Fernanda Medina Monterrey
David Santiago Guerrero García
Universidad de Santander
Programación I
Bucaramanga, Santander
2026
