# MANUAL DIDÁCTICO DEL APRENDIZ — SESIÓN 3
## Gestión para el análisis de los datos depurados
### Evidencia: GA5-220501114-AA1-EV03

**Programa:** Tecnólogo en Gestión del Desarrollo Administrativo e Innovación (122153)
**Fichas:** 3466323 y 3466324 — Modalidad virtual
**Fase del proyecto:** Planeación | Actividad de Proyecto 2 (AP2)
**Instructor:** Julián Andrés Trujillo Morales

---

## 1. Antes de empezar: qué vas a hacer
Este manual está escrito para que puedas **hacer la evidencia sin dudas**, paso a paso. Primero entenderás **qué es analizar** y cómo se elige el método y el gráfico; luego harás en Excel **las medidas de resumen, las tablas dinámicas, los gráficos dinámicos y el dashboard**; y al final escribirás **el plan de gestión y análisis** que se entrega en Zajuna.

> [!verde] **La EV03 en una frase:** con los datos que depuraron en la EV02, planteen **preguntas de negocio**, **caractericen las variables**, calculen **medidas de resumen**, construyan **tablas y gráficos dinámicos** y un **dashboard** en Excel, y escriban un **plan de gestión y análisis** (PDF, máximo 5 páginas) con el enlace de la carpeta de Drive.

| Pregunta | Respuesta |
|---|---|
| ¿Qué entrego? | Dos productos: el **plan de gestión y análisis en PDF** (máximo 5 páginas) que se sube a Zajuna, y el **libro de Excel** `analisis_clientes.xlsx` con tabla dinámica, gráfico dinámico y dashboard, dentro de la subcarpeta **08_analisis_xxx** de Drive. |
| ¿Quién la hace? | Un **equipo de 4 aprendices**. Entregan un solo plan y un solo libro por equipo. |
| ¿Cuándo? | Antes del **miércoles, 18 de noviembre de 2026, 11:59 p. m.** |
| ¿Dónde se entrega? | El **PDF** `EV03_NombreEmpresa.pdf` se sube en **Zajuna**, en el espacio *GA5-220501114-AA1-EV03*. |
| ¿Con quién comparto la carpeta? | Con el instructor: **instructorjuliantrujilo@gmail.com** (permiso *Comentador*). |

> [!naranja] **Qué NO pide la EV03:** modelos de predicción ni estadística avanzada. Se pide **describir y presentar** los datos que ya tienes: medidas de resumen, tabla dinámica, gráfico dinámico, dashboard y un plan que explique cómo y por qué lo hiciste.

### Cómo usar este manual
1. Lee las secciones **2 y 3** para entender qué es analizar, los tipos de variable y cómo se elige el método y el gráfico.
2. Lee la sección **4** para conocer la plantilla y cómo se escribe una fórmula con tablas de Excel.
3. Sigue las secciones **5 a 8** con la plantilla abierta: medidas, tablas dinámicas, gráficos dinámicos y dashboard. Son los mismos pasos de la hoja **LEEME**.
4. Usa la sección **9** para escribir el plan y la **10** para dejar la carpeta en orden.
5. Lee la sección **11** para ver qué pide la guía frase por frase y la **12** para el paso a paso del equipo.
6. Antes de entregar, revisa la **lista de chequeo** (sección 19).

### Dónde encaja esta evidencia
La competencia **220501114 — Sistematizar datos masivos de acuerdo con métodos de analítica y herramientas tecnológicas** se trabaja con la actividad **GA5-220501114-AA1** (72 horas), que evalúa el **RAP 220501114-01**: *Interpretar métodos de analítica de datos de acuerdo con marco legal y modelo de gestión de la organización*.

Volvemos a la cocina: en la EV01 **compraste los ingredientes** y en la EV02 los **lavaste y cortaste**. Hoy, en la EV03, por fin **cocinas**: conviertes los datos limpios en respuestas para quien toma decisiones.

| Evidencia | Qué haces | Analogía |
|---|---|---|
| EV01 | Recolectar información legal y organizada | Comprar los ingredientes |
| EV02 | Sistematizar y depurar los datos | Lavar y cortar |
| **EV03** (hoy) | Gestión para el análisis (estadística, tabla dinámica, dashboard) | Cocinar |
| EV04 | Base de datos final | Servir en el plato |
| EV05 | Cuestionario individual | Probar si quedó bien |

---

## 2. ¿Por qué hay que analizar? Datos limpios no bastan
En la EV02 dejaste las ventas de Lácteos del Valle **limpias y ordenadas**. Ahora el gerente, don Carlos, te hace preguntas: *¿en qué ciudad se vende más?, ¿cuánto vende una venta típica?, ¿hay ventas raras?* Mirar la tabla no responde esas preguntas. Hay tres problemas:

| Problema | Qué pasa | Cómo lo resuelve el análisis |
|---|---|---|
| Mirar no basta | Con 19 filas todavía se puede contar a mano. Con 1.900, no. | Medidas de resumen y tablas dinámicas que resumen en segundos. |
| El promedio engaña | Una sola venta de 650 unidades sube el promedio a 47,9, aunque la venta típica es de 8. | Comparar media y mediana, y explicar los atípicos. |
| Sin gráfico no se comunica | Una tabla de números no se entiende en 10 segundos. | Un gráfico bien elegido y un dashboard con lo importante arriba. |

> [!tech] **Analogía:** tener los ingredientes lavados y cortados **no es tener el plato servido**. Falta cocinarlos con una receta. El análisis es esa receta, y el plan de gestión y análisis es la receta escrita para que cualquiera la pueda repetir.

---

## 3. Conceptos clave explicados con ejemplos

### 3.1. ¿Qué es analizar los datos?
Analizar no es «hacer gráficos». Es **hacerle preguntas a los datos y responderlas con un método**. Se hace en cinco pasos:

| Paso | Qué haces | Ejemplo con la pregunta de don Carlos |
|---|---|---|
| 1. Empieza por la pregunta | Escribe qué necesita saber quien decide, en una pregunta corta y concreta. | «¿En qué ciudad vendemos más?» |
| 2. Mira qué datos tienes | Revisa qué columnas hay y de qué tipo es cada una. | Ciudad (categoría) y Factura (para contar ventas). |
| 3. Elige el método | Decide qué operación responde la pregunta: contar, sumar, promediar, comparar. | Contar ventas por ciudad y calcular el porcentaje. |
| 4. Muestra el resultado | Una tabla para los números exactos y un gráfico para entenderlo de un vistazo. | Tabla dinámica y gráfico de barras ordenado. |
| 5. Ayuda a decidir | El análisis termina cuando alguien puede hacer algo con él. | «Cali concentra 11 de las 17 ventas: conviene reforzar allí la distribución.» |

> [!verde] **Buena pregunta:** «¿En qué ciudad vendemos más?» (concreta, se responde con datos). **Mala pregunta:** «¿Cómo van las ventas?» (demasiado general: ¿en qué, dónde, comparado con qué?).

### 3.2. De la pregunta al gráfico
Cada pregunta se traduce siempre igual: **pregunta → variables → método → gráfico**. Este recorrido es la tabla central de tu plan (hoja `4_Plan` de la plantilla).

| Pregunta | Variables | Método | Gráfico |
|---|---|---|---|
| ¿En qué ciudad se vende más? | Ciudad + Factura | Contar ventas por ciudad y su porcentaje | Barras ordenadas |
| ¿Qué referencia mueve más unidades? | Referencia + Unidades | Sumar unidades por referencia | Columnas |
| ¿Cuánto vende una venta típica? | Unidades | Media, mediana y moda | Cuadro de resumen |
| ¿Hay ventas fuera de lo normal? | Unidades | Mínimo, máximo y comparar con la mediana | Barras ordenadas |
| ¿Cómo se comportan las ventas en el tiempo? | Fecha + Unidades | Sumar unidades por día | Líneas |

### 3.3. Tipos de variable: lo primero que debes saber de cada columna
Caracterizar los datos es decir **de qué tipo es cada columna**. De eso depende qué cuentas puedes hacer.

| Variable | Ejemplo | Tipo | Qué se puede calcular |
|---|---|---|---|
| Ciudad | Cali | Cualitativa nominal | Contar, porcentaje, moda |
| Referencia | LV-002 | Cualitativa nominal | Contar, porcentaje, moda |
| Nivel de satisfacción | Alta | Cualitativa ordinal | Contar, ordenar, mediana |
| Unidades | 8 | Cuantitativa discreta | Suma, media, mediana, moda, mínimo, máximo |
| Peso del pedido (kg) | 12,45 | Cuantitativa continua | Suma, media, mediana, desviación |
| Factura | F-1002 | Identificador | Solo contar (no se suma ni se promedia) |

Para reconocer el tipo, hazte tres preguntas:
1. **¿Es un nombre o un número?** Si responde «¿cuál?» (Cali, LV-002) es **cualitativa**; si responde «¿cuánto?» es **cuantitativa**.
2. **Si es número, ¿se cuenta o se mide?** Si se cuenta (8 unidades) es **discreta**; si se mide (12,45 kg) es **continua**.
3. **Si es categoría, ¿tiene orden?** Cali y Palmira no tienen orden: **nominal**. Baja, media y alta sí: **ordinal**.

> [!naranja] **Ojo con los códigos:** el teléfono o el número de factura **parecen números pero no son cantidades**. Excel deja sumarlos, pero el resultado no significa nada. Se tratan como identificadores.

### 3.4. Elegir el método estadístico: ¿media o mediana?
Piensa en una cafetería con cinco empleados: cuatro ganan cerca de $1.500.000 y el dueño gana $9.000.000.

| Medida | Cómo se calcula | Resultado | ¿Describe a la mayoría? |
|---|---|---|---|
| Media (promedio) | Suma ÷ cantidad = 14.900.000 ÷ 5 | $2.980.000 | No: el sueldo del dueño la sube |
| Mediana | Ordena y toma el del medio | $1.500.000 | Sí |

- Con **categorías** (Ciudad, Referencia) no hay promedio: se **cuentan** y se calcula el **porcentaje**; la moda dice cuál se repite más.
- Con **números** (Unidades) se resume el valor típico con **media, mediana y moda**.
- Si hay **valores extremos**, usa la **mediana** o reporta las dos.

> [!verde] **En tu plan lo justificas con una frase:** «Unidades es cuantitativa discreta y tiene un valor extremo, por eso usamos la mediana como valor típico y reportamos también la media».

### 3.5. Las medidas de resumen
| Medida | Qué dice | Fórmula en Excel |
|---|---|---|
| Recuento | Cuántos datos numéricos hay | `=CONTAR(rango)` |
| Suma | El total | `=SUMA(rango)` |
| Media | Cuánto le toca a cada uno si se reparte por igual | `=PROMEDIO(rango)` |
| Mediana | El valor del medio de los datos ordenados | `=MEDIANA(rango)` |
| Moda | El valor que más se repite | `=MODA.UNO(rango)` |
| Mínimo y máximo | El menor y el mayor | `=MIN(rango)` y `=MAX(rango)` |
| Rango | La distancia entre el mayor y el menor | `=MAX(rango)-MIN(rango)` |
| Desviación estándar | Qué tan separados están los datos de la media | `=DESVEST.M(rango)` |

### 3.6. El dato atípico y el promedio
Las 17 ventas válidas van casi todas de 4 a 12 unidades, pero hay una de 50 y una de **650**. Esa sola venta **empuja la media** hacia arriba:

| Medida | Con la venta de 650 | Sin la venta de 650 |
|---|---|---|
| Media | 47,9 | 10,25 |
| Mediana | 8 | 7,5 |
| Máximo | 650 | 50 |

Qué hacer con un atípico:
1. **Verifica el dato:** revisa la factura o pregunta a quien la capturó.
2. **Decide:** si es real, **se queda y se explica**; si es un error comprobado, se corrige o se excluye con una justificación escrita.
3. **Cuéntalo:** en el plan y en el dashboard, reporta media y mediana y explica el atípico.

> [!naranja] **Nunca escondas un atípico.** En el ejemplo, la venta de 650 es real (un mayorista en Yumbo): se deja y se reportan las dos medidas.

### 3.7. Elegir el gráfico adecuado
| Gráfico | Para qué sirve | Pregunta de ejemplo |
|---|---|---|
| Barras o columnas | Comparar categorías | ¿En qué ciudad se vende más? |
| Circular | Partes de un todo (pocas categorías) | ¿Qué porcentaje de las ventas es de cada ciudad? |
| Líneas | Cambios en el tiempo | ¿Cómo evolucionaron las ventas por día? |
| Histograma | Cómo se reparten los valores de un número | ¿Cuántas ventas son de 0 a 10 unidades, de 11 a 20…? |
| Dispersión | Si dos números se relacionan | ¿Si sube el precio, bajan las unidades? |

> [!tech] **Antes de graficar, respóndete:** 1) ¿qué pregunta responde?, 2) ¿de qué tipo es la variable?, 3) ¿qué debería notar quien lo vea? Usa un color de énfasis, empieza el eje en cero y pon un título que diga la conclusión.

---

## 4. Tu plantilla de Excel y cómo se escribe una fórmula

### 4.1. La plantilla: un libro, siete hojas
Descarga `Plantilla_EV03_Analisis.xlsx` desde el Hub (carpeta **Sesión 3**). También está el **ejemplo resuelto** `Ejemplo_EV03_Dashboard.xlsx` para que compares.

| Hoja | Qué tiene | Qué haces |
|---|---|---|
| `LEEME` | Instrucciones, paso a paso y errores frecuentes | Léela primero: tiene los mismos pasos de este manual |
| `1_Ventas` | Las 19 ventas depuradas de la EV02 como tabla de Excel (`tblVentas`). Dos están marcadas POR VERIFICAR con Incluir = No | Revisas los datos |
| `2_Clientes` | Los 19 clientes depurados (`tblClientes`) | Cuentas clientes por ciudad si lo necesitas |
| `3_Estadisticos` | Las medidas de resumen de Unidades | Escribes las fórmulas en las celdas amarillas |
| `4_Plan` | Caracterización de variables y tabla pregunta → variables → método → gráfico | La completas con las preguntas de tu equipo |
| `5_Tablas_dinamicas` | Hoja en blanco con una guía en la fila 39 | Construyes las 5 tablas dinámicas y los 2 gráficos |
| `6_Dashboard` | Hoja con recuadros para indicadores, gráficos y segmentación | Armas el dashboard |

### 4.2. Un archivo por grupo: original y copia
1. **Guarda el original:** el coordinador sube la plantilla, **sin editarla**, a la carpeta `03_Datos_crudos` de Drive del equipo (la misma de la EV01).
2. **Haz una copia:** en Drive, clic derecho sobre la plantilla ▸ *Hacer una copia*. Crea la subcarpeta `08_analisis_xxx` (por ejemplo `08_analisis_LacteosDelValle`), mueve la copia allí y cámbiale el nombre a `analisis_clientes.xlsx`.
3. **Todos trabajan en la copia.** Las tablas dinámicas, las segmentaciones y el dashboard funcionan mejor en **Excel de escritorio**: trabajen por turnos (descargar, editar, volver a subir y avisar al equipo).

> [!naranja] **Rutas largas:** si descargas la carpeta a tu computador dentro de varias subcarpetas de OneDrive, Excel puede decir que la ruta «es mayor que 259 caracteres». Usa nombres cortos o guarda la carpeta más cerca del escritorio.

### 4.3. Cómo se escribe una fórmula con tablas de Excel (léelo primero)
En la plantilla, los datos están como **tabla de Excel**. Por eso las fórmulas no usan rangos como `C2:C20`, sino el nombre de la tabla y la columna: `tblVentas[Unidades]` significa «la columna Unidades de la tabla de ventas».

1. Haz clic en la **celda amarilla** de la columna C, en la fila de la medida.
2. Escribe `=CONTAR(` y luego `tblV`. Al escribir `tbl`, Excel muestra las tablas del libro (**tblClientes** y **tblVentas**). Escribe hasta la **V** para que quede solo **tblVentas** y pulsa **Tab**.
3. Escribe `[` y Excel muestra las columnas de la tabla. Elige **Unidades** y pulsa **Tab**.
4. Cierra con `)` y pulsa **Enter**.
5. Compara tu resultado con la columna **Resultado esperado**.

> [!tech] **Cómo sacar los corchetes.** Teclado latinoamericano: **Shift + la tecla `{`** (a la derecha de la Ñ) para `[`, y **Shift + `}`** para `]`. Teclado de España: **Alt Gr + `` ` ``** y **Alt Gr + `+`**. En cualquier teclado: **Alt + 91** y **Alt + 93** con el teclado numérico.

> [!naranja] **La columna B solo es la guía.** En `3_Estadisticos` la columna B muestra la fórmula como texto para que la copies. No escribas encima: la fórmula va en la celda amarilla de la columna C.

### 4.4. Errores frecuentes con las fórmulas
| Lo que ves | Por qué pasa | Qué haces |
|---|---|---|
| No aparece la columna Unidades | Elegiste tblClientes en vez de tblVentas | Pulsa Esc y vuelve a escribir `tblV` antes de pulsar Tab |
| `#¿NOMBRE?` | La función o el nombre de la tabla está mal escrito | Usa las sugerencias de Excel; la función va en español |
| La fórmula se ve escrita y no calcula | La celda está en formato Texto | Inicio ▸ Número ▸ General y vuelve a escribirla |
| Error de sintaxis | Tu Excel usa coma en vez de punto y coma | Cambia `;` por `,` (solo en fórmulas con varios argumentos) |

---

## 5. Paso 2 · Las medidas de resumen en Excel
Trabaja en la hoja `3_Estadisticos`. Las ventas POR VERIFICAR son texto y estas funciones las ignoran: por eso se cuentan **17 ventas**, no 19.

### 5.1. Recuento de ventas (celda C2)
```text title="Fórmula para la celda C2" btn="Copiar fórmula"
=CONTAR(tblVentas[Unidades])
```
**Qué hace:** cuenta solo las celdas que tienen número. **Resultado esperado: 17.**

### 5.2. Suma de unidades (celda C3)
```text title="Fórmula para la celda C3" btn="Copiar fórmula"
=SUMA(tblVentas[Unidades])
```
**Qué hace:** suma todas las unidades vendidas; los textos se ignoran. **Resultado esperado: 814.**

### 5.3. Media o promedio (celda C4)
```text title="Fórmula para la celda C4" btn="Copiar fórmula"
=PROMEDIO(tblVentas[Unidades])
```
**Qué hace:** divide la suma entre el recuento (814 ÷ 17). Se infla con ventas muy grandes. **Resultado esperado: 47,88.**

### 5.4. Mediana (celda C5)
```text title="Fórmula para la celda C5" btn="Copiar fórmula"
=MEDIANA(tblVentas[Unidades])
```
**Qué hace:** ordena las ventas y toma la del medio. No se deja afectar por los atípicos. **Resultado esperado: 8.**

### 5.5. Moda (celda C6)
```text title="Fórmula para la celda C6" btn="Copiar fórmula"
=MODA.UNO(tblVentas[Unidades])
```
**Qué hace:** devuelve el valor que más se repite. Si tu Excel no la reconoce, usa `=MODA(tblVentas[Unidades])`. **Resultado esperado: 7.**

### 5.6. Mínimo y máximo (celdas C7 y C8)
```text title="Fórmulas para las celdas C7 y C8" btn="Copiar fórmulas"
=MIN(tblVentas[Unidades])
=MAX(tblVentas[Unidades])
```
**Qué hacen:** la venta más pequeña y la más grande. **Resultados esperados: 4 y 650.**

### 5.7. Rango (celda C9)
```text title="Fórmula para la celda C9" btn="Copiar fórmula"
=MAX(tblVentas[Unidades])-MIN(tblVentas[Unidades])
```
**Qué hace:** resta el mínimo al máximo: muestra qué tan lejos están los extremos. **Resultado esperado: 646.**

### 5.8. Desviación estándar (celda C10)
```text title="Fórmula para la celda C10" btn="Copiar fórmula"
=DESVEST.M(tblVentas[Unidades])
```
**Qué hace:** mide qué tan separados están los datos de la media. Si es mayor que la media, hay atípicos. **Resultado esperado: 155,52.**

### 5.9. Interpreta los resultados
Compara la **media (47,88)** con la **mediana (8)**: están muy separadas porque hay ventas atípicas (50 y 650). Por eso la mediana describe mejor la venta típica. Anota en `4_Plan` y en el plan cómo trataste los atípicos.

> [!verde] **Cómo sabes que quedó bien:** las nueve celdas amarillas coinciden con la columna Resultado esperado.

---

## 6. Paso 3 · Las tablas dinámicas
Una **tabla dinámica** agrupa y resume miles de filas arrastrando los nombres de las columnas a cuatro cajas: **Filtros, Columnas, Filas y Valores**. Vas a crear 5 tablas en la hoja `5_Tablas_dinamicas`: 3 para analizar y 2 que alimentan los gráficos del dashboard. Todas salen de `tblVentas` y todas filtran **Incluir = Sí**.

| Caja | Qué va ahí | Ejemplo |
|---|---|---|
| Filas | Lo que quieres comparar | Ciudad |
| Valores | Lo que quieres calcular | Recuento de Factura, Suma de Unidades |
| Filtros | Lo que dejas fuera | Incluir = Sí |
| Columnas | Opcional: una segunda categoría | Referencia |

### 6.1. Inserta la primera tabla
1. Ve a `1_Ventas` y haz clic en cualquier celda de los datos.
2. **Insertar ▸ Tabla dinámica ▸ Desde una tabla o rango.** Verifica que en *Tabla o rango* diga `tblVentas`.
3. Marca **Hoja de cálculo existente**, haz clic en la pestaña `5_Tablas_dinamicas` y luego en la celda **A4** ▸ **Aceptar**.
4. A la derecha aparece el panel **Campos de tabla dinámica**.

### 6.2. Tabla 1: ventas y unidades por ciudad (A4)
1. Arrastra **Ciudad** a **Filas**.
2. Arrastra **Factura** a **Valores** (queda *Cuenta de Factura*).
3. Arrastra **Unidades** a **Valores**. Si dice *Cuenta de Unidades*: clic en ella ▸ **Configuración de campo de valor ▸ Suma ▸ Aceptar**.
4. Arrastra **Incluir** a **Filtros** y en la celda B2 elige **Sí**.
5. Escribe en B4 `Ventas` y en C4 `Unidades vendidas`.

**Resultado esperado:** Cali 11 y 80 · Palmira 3 y 64 · Yumbo 2 y 659 · Jamundí 1 y 11 · Total 17 y 814.

### 6.3. Ponle nombre a la tabla
Con el cursor dentro de la tabla: **Analizar tabla dinámica ▸ Nombre de tabla dinámica** (a la izquierda) ▸ escribe `tdCiudad` y pulsa Enter. El nombre sirve para reconocerla al conectar la segmentación del dashboard.

### 6.4. Tabla 2: unidades por referencia (G4)
Repite el paso 6.1 con la ubicación **G4**. **Referencia** a Filas, **Unidades** a Valores (Suma) e **Incluir** a Filtros = Sí. Escribe en H4 `Unidades por referencia` y llámala `tdReferencia`.

**Resultado esperado:** LV-001 82 · LV-002 46 · LV-003 686 · Total 814.

### 6.5. Tabla 3: ciudad por referencia (A16)
Repite el paso 6.1 con la ubicación **A16**. **Ciudad** a Filas, **Referencia** a Columnas, **Factura** a Valores (Cuenta) e **Incluir** a Filtros = Sí. Llámala `tdCruzada`.

**Resultado esperado:** una tabla cruzada con Total general 17 (Cali: 4, 4 y 3).

### 6.6. Tabla 4: para el gráfico de ciudades (A32)
Repite el paso 6.1 con la ubicación **A32**. **Ciudad** a Filas, **Factura** a Valores e **Incluir** a Filtros = Sí. Escribe en B32 `Número de ventas`. Ordena: clic derecho sobre un número ▸ **Ordenar ▸ De mayor a menor**. Llámala `pgCiudad`.

### 6.7. Tabla 5: para el gráfico de referencias (G32)
Repite el paso 6.1 con la ubicación **G32**. **Referencia** a Filas, **Unidades** a Valores (Suma) e **Incluir** a Filtros = Sí. Llámala `pgReferencia`.

> [!tech] **¿Por qué las tablas 4 y 5 van aparte?** Un gráfico dinámico cambia la tabla de la que sale (orden, filtros, formato). Con tablas propias para los gráficos, las tablas de análisis no se alteran.

> [!verde] **Otras preguntas con la misma tabla:** para ver el porcentaje de cada ciudad, en Valores: **Configuración de campo de valor ▸ Mostrar valores como ▸ % del total general**. Para ver qué ventas forman un número, haz **doble clic** sobre él.

---

## 7. Paso 4 · Los gráficos dinámicos
Un **gráfico dinámico** está conectado a su tabla dinámica: si filtras la tabla, el gráfico cambia. Vas a crear 2 gráficos, uno desde `pgCiudad` y otro desde `pgReferencia`.

### 7.1. Gráfico de ventas por ciudad
1. Haz clic dentro de la tabla **pgCiudad** (A32).
2. **Analizar tabla dinámica ▸ Gráfico dinámico ▸ Columna ▸ Columna agrupada ▸ Aceptar.**
3. Haz clic en el título y escribe la conclusión: `Cali concentra 11 de las 17 ventas válidas`.
4. Quita la leyenda: botón **+** al lado del gráfico ▸ desmarca **Leyenda**. Si quieres, marca **Etiquetas de datos**.

### 7.2. Gráfico de unidades por referencia
1. Haz clic dentro de la tabla **pgReferencia** (G32).
2. **Gráfico dinámico ▸ Columna agrupada ▸ Aceptar.**
3. Título: `Unidades por referencia (LV-003 incluye el atípico de 650)`. Quita la leyenda.

### 7.3. Lleva los gráficos al dashboard
Los dos gráficos quedaron en la hoja `5_Tablas_dinamicas`. Muévelos uno por uno:
1. **Gráfico de ventas por ciudad** (paso 7.1): haz clic en su borde ▸ pestaña **Diseño de gráfico ▸ Mover gráfico ▸ Objeto en: 6_Dashboard ▸ Aceptar**. En `6_Dashboard` arrástralo sobre el recuadro **Gráfico dinámico 1 (celda B8)**.
2. **Gráfico de unidades por referencia** (paso 7.2): repite lo mismo y ubícalo sobre el recuadro **Gráfico dinámico 2 (celda H8)**.
3. Ajusta ambos al mismo tamaño arrastrando sus esquinas.

> [!tech] **Un gráfico claro:** ordenado de mayor a menor, con un título que diga el mensaje, sin leyenda si hay una sola serie y con un solo color de énfasis. Para ocultar los botones grises: **Analizar gráfico dinámico ▸ Botones de campo**.

---

## 8. Paso 5 · El dashboard
Un **dashboard** junta en **una sola pantalla** los indicadores y los gráficos que responden las preguntas. Tres principios: **una sola pantalla**, **lo importante arriba** y **pocos gráficos y pocos colores** (2 a 4 gráficos, 2 o 3 colores).

### 8.1. Título
En `6_Dashboard`, celda B2: `Dashboard · Lácteos del Valle S.A.S. · octubre 2026` (con el nombre de tu empresa y el periodo). Si quieres, quita la cuadrícula: **Vista ▸ desmarca Líneas de cuadrícula**.

### 8.2. Indicadores clave
| Celda | Título (fila 4) | Fórmula (fila 5) | Resultado |
|---|---|---|---|
| B4 / B5 | Ventas válidas | `=CONTAR.SI(tblVentas[Incluir];"Sí")` | 17 |
| F4 / F5 | Unidades vendidas | `=SUMAR.SI(tblVentas[Incluir];"Sí";tblVentas[Unidades])` | 814 |
| I4 / I5 | Mediana por venta | `=MEDIANA(tblVentas[Unidades])` | 8 |

```text title="Fórmulas de los indicadores" btn="Copiar fórmulas"
=CONTAR.SI(tblVentas[Incluir];"Sí")
=SUMAR.SI(tblVentas[Incluir];"Sí";tblVentas[Unidades])
=MEDIANA(tblVentas[Unidades])
```
Pon los números grandes (tamaño 24) y en negrita. Recuerda escribir `tblV` y pulsar Tab para que Excel complete `tblVentas`.

### 8.3. Segmentación de datos por ciudad
Haz clic en uno de los gráficos ▸ **Analizar gráfico dinámico ▸ Insertar segmentación de datos** ▸ marca **Ciudad** ▸ **Aceptar**. Ubícala en el recuadro de la celda **B24**.

### 8.4. Conecta la segmentación a todas las tablas
Haz clic en la segmentación ▸ pestaña **Segmentación ▸ Conexiones de informe** ▸ marca las 5 tablas (`tdCiudad`, `tdReferencia`, `tdCruzada`, `pgCiudad`, `pgReferencia`) ▸ **Aceptar**.

### 8.5. Prueba y guarda
Haz clic en **Cali** en la segmentación: los gráficos y las tablas dinámicas se filtran. Los 3 indicadores no cambian porque son fórmulas sobre toda la tabla. Para quitar el filtro, usa el embudo con X de la segmentación. Guarda el libro y súbelo a `08_analisis_xxx` como `analisis_clientes.xlsx`.

> [!verde] **Cómo sabes que quedó bien:** el dashboard se ve completo sin desplazarte, tiene título, 3 indicadores, 2 gráficos con título que dice la conclusión y una segmentación que filtra los dos gráficos.

---

## 9. El plan de gestión y análisis
La guía pide un documento que describa **los procedimientos, la caracterización de los datos y el manejo y control de la información**, con el método estadístico y los gráficos elegidos. Es como **la receta de un plato**: quien la lea debe poder repetir el análisis y entender por qué se hizo así.

### 9.1. Las seis secciones del plan
| Sección | Pregunta que responde | De dónde sale |
|---|---|---|
| 1. Introducción y objetivo | ¿Qué quiero saber y por qué? | La pregunta de negocio y la empresa de la EV01 |
| 2. Caracterización de los datos | ¿Con qué datos cuento? | Tabla A de `4_Plan` y la hoja `4_Criterios` de la EV02 |
| 3. Procedimientos | ¿Cómo los preparé y analicé? | Matriz de la EV01, registro de la EV02, columna Incluir y los pasos de este manual |
| 4. Manejo y control de la información | ¿Cómo cuido la información? | Carpetas de Drive, permisos, respaldo y soportes legales de la EV01 |
| 5. Método y gráficos | ¿Qué método y qué gráficos usé, y por qué? | Tabla B de `4_Plan` |
| 6. Dashboard y hallazgos | ¿Qué encontré? | Hojas `3_Estadisticos` y `6_Dashboard` |

### 9.2. Completa la hoja 4_Plan
1. **Tabla A (caracterización):** para cada variable escribe el tipo, un ejemplo, la regla de calidad y para qué se usa.
2. **Tabla B (preguntas):** escribe **al menos tres preguntas** con sus variables, método, gráfico y una frase que justifique la elección.
3. Las filas en gris son ejemplos: reemplázalas por las de tu equipo.

### 9.3. Manejo y control: una frase por cada riesgo
| ¿Qué pasaría si…? | Protección | Qué escribes en el plan |
|---|---|---|
| Se daña el archivo | Respaldo 3-2-1 y todo en Drive | «Los archivos se guardan en Drive con copia en…» |
| Alguien cambia un dato | Historial de versiones y registro de cambios | «Cada cambio se registra en…» |
| Entra quien no debe | Permisos: instructor Comentador, equipo Editor | «El instructor tiene permiso de Comentador…» |
| Hay datos de personas | Ley 1581 de 2012: datos ficticios o anonimizados | «No se usan datos personales reales…» |
| Nadie sabe quién hace qué | Roles definidos | «El coordinador…, el analista…» |
| No se encuentra el archivo | Un solo lugar: `08_analisis_xxx` | «El libro de análisis está en…» |

### 9.4. Plantilla del documento
Copia la plantilla en Google Docs o Word (Arial 11 o 12) y reemplaza lo que está entre corchetes. **Máximo 5 páginas.**

```text title="Plantilla del plan de gestión y análisis" btn="Copiar plantilla"
SERVICIO NACIONAL DE APRENDIZAJE – SENA
Tecnólogo en Gestión del Desarrollo Administrativo e Innovación
Ficha: [3466323 o 3466324]

EVIDENCIA GA5-220501114-AA1-EV03
Plan de gestión y análisis de datos

EMPRESA DE LA EV01: [nombre de la empresa que eligió tu equipo]

INTEGRANTES (si trabajas solo, deja una sola fila)
1. [Nombre completo] – [documento] – Rol: [coordinador]
2. [Nombre completo] – [documento] – Rol: [analista estadístico]
3. [Nombre completo] – [documento] – Rol: [responsable de gráficos y dashboard]
4. [Nombre completo] – [documento] – Rol: [responsable del plan y el control]

Instructor: Julián Andrés Trujillo Morales
Fecha de entrega: [día de mes de año]
------------------------------------------------------------
1. INTRODUCCIÓN Y OBJETIVO DEL ANÁLISIS
[Qué empresa, qué datos y qué preguntas de negocio quieren responder]

2. CARACTERIZACIÓN DE LOS DATOS
[Tabla: variable, tipo, ejemplo, regla de calidad (tabla A de 4_Plan)]

3. PROCEDIMIENTOS
[Cómo se recolectaron (EV01), cómo se depuraron (EV02), qué criterio de inclusión usaron (columna Incluir) y cómo se analizaron en Excel]

4. MANEJO Y CONTROL DE LA INFORMACIÓN
[Dónde se guarda, respaldo, versiones, permisos, marco legal y responsables]

5. MÉTODO ESTADÍSTICO Y GRÁFICOS SELECCIONADOS
[Tabla: pregunta, variables, método, gráfico y por qué (tabla B de 4_Plan)]

6. DASHBOARD Y HALLAZGOS
[Qué muestran las medidas y el dashboard, cómo trataron los atípicos y qué recomiendan]

CARPETA DE DRIVE CON LA EVIDENCIA
Enlace: [pegar enlace]
Compartida con instructorjuliantrujilo@gmail.com (permiso Comentador)
```

---

## 10. La carpeta del equipo: dónde queda todo
Se trabaja **en la misma carpeta de Drive de la EV01**. La EV03 solo agrega la plantilla original en `03_Datos_crudos` y la subcarpeta `08_analisis_xxx`. Todo archivo llega **primero a datos crudos** y luego se copia a la carpeta que le corresponde.

```text title="Carpeta completa del equipo y evidencia de cada parte" btn="Copiar árbol"
EV01_Recoleccion_[Empresa]_Equipo[N]/        (carpeta raíz · EV01 a EV03)
├── 00_LEEME.txt                         EV01
├── 00_Gestion_del_equipo/               EV01
├── 01_Empresa_y_contexto/               EV01
├── 02_Sistemas_de_gestion/              EV01
│   ├── 01_Calidad/
│   ├── 02_Ambiental/
│   ├── 03_SST/
│   └── 04_Seguridad_Informacion/        (solo si la empresa lo tiene)
├── 03_Datos_crudos/                     todo llega primero aquí, sin modificar
│   ├── (datos descargados)              EV01
│   ├── Plantilla_EV02_Depuracion.xlsx   EV02
│   └── Plantilla_EV03_Analisis.xlsx     EV03
├── 04_Matriz_de_recoleccion.xlsx        EV01
├── 05_Soportes_legales/                 EV01
├── 06_Registro_de_depuracion.xlsx       EV02
├── 07_sistematizado_[xxx]/              EV02
│   └── sistematizado_clientes.xlsx
└── 08_analisis_[xxx]/                   EV03 (NUEVO)
    └── analisis_clientes.xlsx
```

| Elemento | Qué va dentro | Detalle |
|---|---|---|
| `03_Datos_crudos/Plantilla_EV03_Analisis.xlsx` | La plantilla original, tal como se descargó | No se abre para trabajar |
| `08_analisis_[xxx]/` | La subcarpeta del análisis | Empieza por «08_analisis_» y termina con una palabra corta: `08_analisis_LacteosDelValle` |
| `analisis_clientes.xlsx` | La copia de la plantilla con todo el trabajo | Medidas, tablas dinámicas, gráficos y dashboard |

> [!tech] **No muevas ni borres nada de la EV01 ni de la EV02.** Quien abra tu carpeta debe poder seguir el recorrido completo: datos crudos → datos depurados → análisis.

---

## 11. La evidencia EV03 explicada frase por frase
| Lo que dice la guía | Qué significa | Ejemplo |
|---|---|---|
| *«Se realizará un análisis completo de información recolectada en las evidencias anteriores»* | Analizas los datos que recolectaste (EV01) y depuraste (EV02). | Hojas `1_Ventas` y `2_Clientes` |
| *«Utilizando las herramientas estadísticas para estructurar la información»* | Aplicas medidas de resumen y tablas dinámicas en Excel. | Media, mediana, moda y tabla dinámica |
| *En equipo de 4 aprendices* | Se reparten roles. | Coordinador, analista, gráficos y dashboard, plan y control |
| *«Elaboren un plan de gestión para el análisis de datos, documentando los procedimientos, caracterización de datos, manejo y control de información»* | Un documento con esas partes. | El plan de 6 secciones, máximo 5 páginas |
| *«Seleccionen el método estadístico más acertado… según su tipo (discreto, continuo, cuantitativo o cualitativo)»* | Caracterizas las variables y eliges el método que corresponde. | Unidades es discreta: media, mediana y moda |
| *«Seleccionen del abanico de herramientas gráficas, las más acertadas»* | Eliges el gráfico según la pregunta y justificas por qué. | Barras para comparar ciudades |
| *«Elaboren una tabla y un gráfico dinámico, relacionado con un dashboard»* | Construyes tabla dinámica, gráfico dinámico y un dashboard conectado. | Hojas `5_Tablas_dinamicas` y `6_Dashboard` |
| **Producto:** plan (PDF, máx. 5 páginas) + tabla, gráfico dinámico y dashboard | Dos entregables: el documento y el libro de Excel. | `EV03_NombreEmpresa.pdf` y `analisis_clientes.xlsx` |
| *«Envío en el espacio GA5-220501114-AA1-EV03»* | Entregas en Zajuna. | El PDF, con el enlace a la carpeta |

---

## 12. Paso a paso para construir la EV03
Estos son los nueve pasos del equipo, en orden. Sigue el orden para no repetir trabajo.

### Paso 1: Reúnanse y repartan los roles
**Qué debes hacer:** repartir los cuatro roles: coordinador, analista estadístico, responsable de gráficos y dashboard, y responsable del plan y el control.
**Cómo sabes que quedó bien:** cada integrante sabe qué parte hace.

### Paso 2: Suban la plantilla a Drive
**Qué debes hacer:** subir el original a `03_Datos_crudos` y la copia a `08_analisis_xxx` como `analisis_clientes.xlsx` (sección 4.2).
**Cómo sabes que quedó bien:** hay un original intacto y una sola copia de trabajo.

### Paso 3: Definan las preguntas del análisis
**Qué debes hacer:** escribir al menos tres preguntas en la tabla B de `4_Plan` (sección 3.2).
**Cómo sabes que quedó bien:** cada pregunta es concreta y se responde con columnas que existen.

### Paso 4: Caractericen las variables
**Qué debes hacer:** completar la tabla A de `4_Plan` con el tipo de cada variable (sección 3.3).
**Cómo sabes que quedó bien:** cada variable tiene tipo, ejemplo y regla de calidad.

### Paso 5: Calculen las medidas de resumen
**Qué debes hacer:** escribir las fórmulas en `3_Estadisticos` y comparar media y mediana (sección 5).
**Cómo sabes que quedó bien:** las celdas amarillas coinciden con el resultado esperado y decidieron qué hacer con los atípicos.

### Paso 6: Construyan las tablas y los gráficos dinámicos
**Qué debes hacer:** las 5 tablas y los 2 gráficos de las secciones 6 y 7.
**Cómo sabes que quedó bien:** los totales dan 17 ventas y 814 unidades, y cada gráfico tiene un título con la conclusión.

### Paso 7: Armen el dashboard
**Qué debes hacer:** título, indicadores, gráficos y segmentación conectada (sección 8).
**Cómo sabes que quedó bien:** al filtrar una ciudad, los dos gráficos cambian.

### Paso 8: Escriban el plan
**Qué debes hacer:** las seis secciones con la plantilla de la sección 9.4, máximo 5 páginas, con el enlace de la carpeta.
**Cómo sabes que quedó bien:** cada método y cada gráfico tiene su justificación.

### Paso 9: Revisen, compartan y entreguen
**Qué debes hacer:** revisar con el checklist (sección 19), compartir la carpeta con el instructor, probar el enlace en incógnito, descargar el plan en PDF y subirlo a Zajuna.
**Cómo sabes que quedó bien:** el PDF se llama `EV03_NombreEmpresa.pdf` y el enlace abre sin iniciar sesión.

---

## 13. Ejemplo resuelto: una EV03 de principio a fin
> [!naranja] **Aviso:** la empresa **«Lácteos del Valle S.A.S.» es ficticia**. Sus datos son los mismos para todos los grupos. Descarga `Ejemplo_EV03_Dashboard.xlsx` desde el Hub para ver el libro terminado.

| Parte | Cómo quedó en el ejemplo |
|---|---|
| Preguntas | ¿En qué ciudad se vende más? ¿Qué referencia mueve más unidades? ¿Cuánto vende una venta típica? |
| Caracterización | Ciudad y Referencia: cualitativas nominales. Unidades: cuantitativa discreta. Fecha: temporal. Factura: identificador |
| Medidas | 17 ventas válidas, 814 unidades, media 47,88, mediana 8, moda 7, mínimo 4, máximo 650, desviación 155,52 |
| Atípicos | La venta de 650 (Yumbo) es real: se deja y se reportan media y mediana. Las 2 ventas POR VERIFICAR quedan fuera con Incluir = No |
| Tablas dinámicas | tdCiudad (A4), tdReferencia (G4), tdCruzada (A16), pgCiudad (A32) y pgReferencia (G32) |
| Gráficos | «Cali concentra 11 de las 17 ventas válidas» y «Unidades por referencia (LV-003 incluye el atípico de 650)» |
| Dashboard | Título, 3 indicadores (17, 814 y 8), 2 gráficos y segmentación por ciudad conectada a las 5 tablas |
| Hallazgo | Cali concentra la mayoría de las ventas; por unidades, Yumbo y LV-003 lideran por una sola venta mayorista |

---

## 14. El PDF de entrega
En Zajuna **se sube el plan en PDF**. A diferencia de la EV01 y la EV02, en la EV03 el PDF **no es solo una portada**: es el plan completo, con el enlace de la carpeta donde está el Excel.

1. Escribe el plan con la plantilla de la sección 9.4.
2. Revisa que tenga **máximo 5 páginas**.
3. Pega el **enlace de la carpeta** y haz clic en él para comprobar que abre en una ventana de incógnito.
4. Descárgalo: **Archivo ▸ Descargar ▸ Documento PDF** (en Word: **Archivo ▸ Guardar como ▸ PDF**).
5. Nómbralo con el nombre de la empresa: `EV03_NombreEmpresa.pdf`, por ejemplo `EV03_LacteosDelValle.pdf`. Sin tildes, sin espacios y sin símbolos.
6. Súbelo en Zajuna, en el espacio *GA5-220501114-AA1-EV03*.

> [!naranja] Los nombres de **todos los integrantes** van dentro de la portada, no en el nombre del archivo.

---

## 15. Cómo se evalúa la evidencia y cómo dejarlo evidenciado
| Indicador del instrumento | Cómo lo dejas evidenciado |
|---|---|
| 1.1 Utiliza información relevante para la organización | La introducción del plan dice qué pregunta de negocio se responde y por qué esos datos importan. |
| 1.2 Son claros los campos (columnas con información caracterizada) | La tabla de caracterización: nombre, tipo, ejemplo y regla de calidad de cada variable. |
| 1.3 La información está libre de sesgo e independiente para su análisis | Datos depurados en la EV02 y un criterio escrito de qué entra y qué no (columna Incluir). Los atípicos se explican. |
| 1.4 La segmentación es adecuada | Cada tabla dinámica usa el segmento que corresponde a su pregunta (ventas o clientes). |
| 2.1 Evidencia en el formato sugerido | Plan en PDF (máx. 5 páginas) y libro de Excel con tabla dinámica, gráfico dinámico y dashboard. |
| 2.2 Usa la web y la nube en carpetas y subcarpetas | Todo en Drive, en la carpeta de la EV01 con la subcarpeta `08_analisis_xxx`. |
| 3.1 Normativa: permisos y cumplimiento de normas | Carpeta compartida con el instructor (Comentador), sin datos personales reales y con el manejo y control descrito en el plan. |

---

## 16. Errores frecuentes y cómo evitarlos
| Error | Cómo evitarlo |
|---|---|
| La tabla dinámica propone Recuento en vez de Suma | La columna tiene texto mezclado (POR VERIFICAR). Cámbiala a Suma en Configuración de campo de valor y filtra Incluir = Sí. |
| El total no da 17 ventas o 814 unidades | Falta el filtro: arrastra Incluir a Filtros y elige Sí. |
| Excel creó una hoja nueva para la tabla | Marcaste Nueva hoja de cálculo. Borra esa hoja y repite eligiendo Hoja de cálculo existente. |
| La segmentación no filtra todos los gráficos | Clic en la segmentación ▸ Conexiones de informe ▸ marca las 5 tablas. |
| La tabla dinámica no cambia al editar los datos | Datos ▸ Actualizar todo. |
| Se usa la media con un atípico sin explicarlo | Reporta media y mediana y explica el atípico en el plan. |
| El plan pasa de 5 páginas | Acorta los párrafos y deja las tablas. |
| Dashboard sin tabla ni gráfico dinámico detrás | Los gráficos del dashboard deben salir de tablas dinámicas, no dibujarse a mano. |
| El enlace pide iniciar sesión | Compártelo como «Cualquier persona con el enlace» y pruébalo en incógnito. |

---

## 17. Preguntas frecuentes
**¿Puedo usar Power BI en vez de Excel?**
La guía permite Excel, Power BI u hoja de cálculo. En la sesión trabajamos con Excel porque es el que todos tenemos.

**¿Cuántas preguntas debo plantear?**
Al menos tres, con su variable, método y gráfico. Más preguntas no mejoran la nota si el plan pasa de 5 páginas.

**¿Qué hago si mi equipo depuró distinto en la EV02?**
Usa tus datos: pégalos en `1_Ventas` y `2_Clientes`, ajusta la columna Incluir y anota las diferencias en el plan.

**¿Qué hago con un valor atípico?**
Verifícalo. Si es real, déjalo y reporta media y mediana; si es un error comprobado, exclúyelo y justifícalo en el plan.

**¿Por qué los indicadores del dashboard no cambian con la segmentación?**
Porque son fórmulas sobre toda la tabla `tblVentas`. La segmentación solo filtra tablas y gráficos dinámicos.

**¿Puedo trabajar en Hojas de cálculo de Google?**
Para las fórmulas sí. Las tablas dinámicas, las segmentaciones y el dashboard funcionan mejor en Excel de escritorio.

---

## 18. Plan de trabajo sugerido
| Fecha | Qué hacer | Resultado |
|---|---|---|
| Martes 10 de noviembre (Sesión 3) | Descargar la plantilla, subirla a Drive y repartir roles | Plantilla en `08_analisis_xxx` |
| Miércoles 11 de noviembre | Entregar la EV02 | EV02 entregada |
| Jueves 12 – sábado 14 | Definir preguntas, caracterizar variables y calcular medidas | Hojas `3_Estadisticos` y `4_Plan` |
| Domingo 15 – lunes 16 | Tablas y gráficos dinámicos, dashboard y plan | Libro y plan listos |
| Martes 17 de noviembre (Sesión 4) | Resolver dudas de la EV01 a la EV03 | Observaciones |
| Miércoles 18 de noviembre | Entregar en Zajuna (mejor un día antes) | EV03 entregada |

> [!tech] **Consejo:** no dejen la entrega para el último minuto. Si el enlace falla o falta un gráfico, necesitarán tiempo para corregirlo.

---

## 19. Lista de chequeo anti-rechazo
Marca cada casilla antes de subir tu evidencia a Zajuna:

- [ ] La plantilla original está en `03_Datos_crudos` sin modificar — Y la copia de trabajo está en `08_analisis_xxx` como analisis_clientes.xlsx.
- [ ] Las medidas de resumen están calculadas — Las celdas amarillas de 3_Estadisticos coinciden con el resultado esperado.
- [ ] Cada variable tiene su tipo — Cualitativa (nominal u ordinal), cuantitativa discreta o continua.
- [ ] El método está justificado — Una frase por pregunta: «Unidades es discreta, por eso…».
- [ ] Hay tablas dinámicas — Con el filtro Incluir = Sí y totales de 17 ventas y 814 unidades.
- [ ] Hay gráficos dinámicos — Con título que dice la conclusión, conectados al dashboard.
- [ ] El dashboard está completo — Título, indicadores, gráficos y segmentación conectada.
- [ ] Los atípicos están explicados — Con la decisión que tomó el equipo.
- [ ] El plan tiene máximo 5 páginas — Con las seis secciones y en PDF.
- [ ] La carpeta está compartida con el instructor — Permiso Comentador a instructorjuliantrujilo@gmail.com.
- [ ] El enlace abre sin iniciar sesión — Probado desde una ventana de incógnito.
- [ ] El PDF se llama EV03_NombreEmpresa.pdf — Con los nombres de todos los integrantes en la portada.

---

## 20. Glosario
| Término | Significado |
|---|---|
| Analizar | Hacerle preguntas a los datos y responderlas con un método. |
| Variable | Cada columna de la tabla: una característica que cambia de una fila a otra. |
| Cualitativa | Variable que es una categoría o un nombre (Ciudad). |
| Cuantitativa discreta | Número que resulta de contar (Unidades). |
| Cuantitativa continua | Número que resulta de medir y admite decimales (peso). |
| Media | Suma de los valores dividida entre la cantidad. |
| Mediana | El valor del medio de los datos ordenados. |
| Moda | El valor que más se repite. |
| Desviación estándar | Qué tan separados están los datos de la media. |
| Atípico | Valor muy distinto del resto, que puede ser real o un error. |
| Tabla de Excel | Rango con formato de tabla (Ctrl+T) y nombre propio, como tblVentas. |
| Tabla dinámica | Herramienta de Excel que agrupa y resume datos arrastrando campos. |
| Gráfico dinámico | Gráfico conectado a una tabla dinámica: cambia cuando ella cambia. |
| Segmentación de datos | Botones para filtrar tablas y gráficos dinámicos con un clic. |
| Dashboard | Pantalla única con indicadores y gráficos que responden las preguntas. |
| Plan de gestión y análisis | Documento que describe procedimientos, caracterización, manejo y control, método y hallazgos. |

---

## 21. Referencias
- Guía de aprendizaje 5 — Competencia 220501114, actividad GA5-220501114-AA1 (disponible en el Hub).
- Instrumento de evaluación IE-GA5-220501114-AA1-EV03 — Gestión para el análisis de datos.
- Presentación de la Sesión 3, plantilla `Plantilla_EV03_Analisis.xlsx` y ejemplo resuelto `Ejemplo_EV03_Dashboard.xlsx` (disponibles en el Hub).
- Ley 1581 de 2012 — Protección de datos personales en Colombia.
- Microsoft. *Ayuda de Excel*: Crear una tabla dinámica, Crear un gráfico dinámico y Usar segmentaciones de datos.

---

*Manual didáctico para los aprendices de la Ficha 3466323 y 3466324 — Gestión del Desarrollo Administrativo e Innovación. Instructor: Julián Andrés Trujillo Morales.*
