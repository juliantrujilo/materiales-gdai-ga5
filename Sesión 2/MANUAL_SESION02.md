# MANUAL DIDÁCTICO DEL APRENDIZ — SESIÓN 2
## Sistematización y depuración de los datos recopilados
### Evidencia: GA5-220501114-AA1-EV02

**Programa:** Tecnólogo en Gestión del Desarrollo Administrativo e Innovación (122153)
**Fichas:** 3466323 y 3466324 — Modalidad virtual
**Fase del proyecto:** Planeación | Actividad de Proyecto 2 (AP2)
**Instructor:** Julián Andrés Trujillo Morales

---

## 1. Antes de empezar: qué vas a hacer
Este manual está escrito para que puedas **hacer la evidencia sin dudas**, paso a paso. Primero entenderás **por qué** hay que limpiar los datos, luego aprenderás **cómo** hacerlo en Excel y, al final, verás **qué pide exactamente la evidencia**.

> [!verde] **La EV02 en una frase:** tomen el conjunto de datos de la plantilla de Excel, **límpienlo y organícenlo con reglas claras** (quitar repetidos, unificar formatos, tratar vacíos y valores raros), sepárenlo en **tablas por segmento**, anoten **todo lo que hicieron en un registro** y entreguen en Zajuna un **PDF con portada, introducción y enlace** de la carpeta de Drive.

| Pregunta | Respuesta |
|---|---|
| ¿Qué entrego? | Una carpeta de Drive con la subcarpeta **07_sistematizado_xxx** (la plantilla de Excel ya trabajada), el archivo de control **06_Registro_de_depuracion.xlsx** y, en Zajuna, un **PDF de entrega** (portada, introducción y enlace). |
| ¿Con qué datos trabajo? | Con la **plantilla de Excel** de la sesión: 24 clientes de una empresa ficticia (Lácteos del Valle S.A.S.). **Todos los grupos usan los mismos datos**, porque muchas empresas no publican los datos de sus clientes. |
| ¿Quién la hace? | Un **equipo de 4 aprendices** o, si lo prefieres, **de forma individual**. Entregan un solo archivo de trabajo por grupo. |
| ¿Cuándo se entrega? | Antes del **miércoles, 11 de noviembre de 2026, 11:59 p. m.** |
| ¿Dónde se entrega? | El **PDF** `EV02_NombreEmpresa.pdf` se sube en **Zajuna**, en el espacio *GA5-220501114-AA1-EV02 — Sistematización de datos recopilados*. |
| ¿Con quién comparto la carpeta? | Con el instructor: **instructorjuliantrujilo@gmail.com** (permiso *Comentador*). |
| ¿Con qué herramienta? | **Excel**: es amigable y la tenemos todos. La guía también permite Access o Power BI. |
| ¿Cómo me evalúan? | Con la lista de chequeo **IE-GA5-220501114-AA1-EV02** (sección 11). |

> [!naranja] **Qué NO pide la EV02:** análisis. Nada de promedios, tablas dinámicas, gráficos ni conclusiones: eso es la **EV03**. En la EV02 dejas los datos **limpios, ordenados y documentados**.

### Cómo usar este manual
1. Lee las secciones **2 a 4** para entender los conceptos y cómo se aplica una fórmula.
2. Sigue la sección **5** problema por problema, con la plantilla de Excel abierta.
3. Sigue la sección **6** para segmentar, llevar el registro y organizar la carpeta.
4. Lee la sección **7** para ver qué pide la guía frase por frase y la **8** para el paso a paso del equipo.
5. Compara tu avance con el **ejemplo resuelto** (sección 9).
6. Arma el **PDF de entrega** con la sección 10 y revisa la **lista de chequeo** (sección 15) antes de entregar.

### Dónde encaja esta evidencia
La competencia **220501114 — Sistematizar datos masivos de acuerdo con métodos de analítica y herramientas tecnológicas** se trabaja con la actividad **GA5-220501114-AA1** (72 horas), que evalúa el **RAP 220501114-01**: *Interpretar métodos de analítica de datos de acuerdo con marco legal y modelo de gestión de la organización*.

Volvemos a la cocina: en la EV01 **compraste los ingredientes**. Hoy, en la EV02, los **lavas, pelas y cortas**. Todavía no cocinas: eso es la EV03. Si cocinas con ingredientes sucios, el plato sale mal por más buena que sea la receta.

| Evidencia | Qué haces | Analogía |
|---|---|---|
| EV01 | Recolectar información legal y organizada | Comprar los ingredientes |
| **EV02** (hoy) | Sistematizar y depurar los datos | Lavar y cortar |
| EV03 | Gestión para el análisis (estadística, tabla dinámica, dashboard) | Cocinar |
| EV04 | Base de datos final | Servir en el plato |
| EV05 | Cuestionario individual | Probar si quedó bien |

---

## 2. ¿Por qué hay que sistematizar? Datos sucios, decisiones equivocadas
Mira esta tabla de clientes (son las **primeras 8 filas** de la plantilla). Parece normal, pero tiene problemas que hacen que cualquier cifra salga mal.

| ID | Nombres | Apellidos | Teléfono | Correo | Ciudad |
|---|---|---|---|---|---|
| 1 | ana maría | PÉREZ | 3105551234 | ana.perez@mail.com | Cali |
| 2 | Ana María | Pérez | 310 555 1234 | ana.perez@mail.com | cali |
| 3 | Luis | Gómez | 3105559876 | luis.gomez@mail | Cali |
| 4 | Marta | Rojas | *(vacío)* | marta.rojas@mail.com | Santiago de Cali |
| 5 | Pedro | Díaz | +57 320 555 1111 | *(vacío)* | Palmira |
| 6 | Juana | Ríos | 3205552222 | juana.rios@mail.com | CALI |
| 7 | pedro | Díaz | 320 555 1111 | pedro.diaz@mail.com | Palmira |
| 8 | Luis | Gómez | 3105559876 | luis.gomez@mail | Cali |

El informe de gerencia dice «8 clientes». **Pregunta para pensar:** ¿cuántos clientes **distintos** hay? La respuesta es **5**: Ana María Pérez, Luis Gómez, Marta Rojas, Pedro Díaz y Juana Ríos. Las otras tres filas son repeticiones.

Este desorden tiene tres consecuencias:
1. **Cuentas mal:** hay 8 filas pero solo 5 personas. El informe infla la cifra en 60 %.
2. **Contactas mal:** los teléfonos están escritos de tres maneras, Marta no tiene teléfono y el correo de Luis está incompleto. Una campaña de mensajes no llega a todos.
3. **Decides mal:** un reporte por ciudad contaría «Cali», «cali», «CALI» y «Santiago de Cali» como **cuatro ciudades distintas**.

> [!tech] **Analogía:** es como **beber agua turbia**. El agua existe, pero antes de tomarla la filtras. Depurar es filtrar los datos antes de usarlos. «Basura entra, basura sale»: un análisis solo es tan bueno como los datos con que se alimenta.

---

## 3. Conceptos clave explicados con ejemplos

### 3.1. ¿Qué es sistematizar?
Sistematizar es dejar la información **ordenada, limpia y organizada con reglas** para que se pueda usar. La guía dice que la sistematización debe cumplir tres verbos:

| Verbo | Qué significa | Ejemplo |
|---|---|---|
| **Clasificar** | Poner cada información en su lugar según los lineamientos de la organización (por área, departamento o sistema de gestión). | Los datos de clientes van en una tabla y los de productos en otra. |
| **Caracterizar** | Describir cada dato: qué es, de qué tipo, en qué formato y para qué lo necesita la organización. | La columna Teléfono es texto de 10 dígitos y sirve para contactar al cliente. |
| **Estructurar** | Dejar los datos en tablas: una fila por cada cosa y una columna por cada característica, siempre que sea posible. | Una fila por cliente; columnas ID, Nombres, Apellidos, Teléfono, Correo, Ciudad. |

Piensa en una **biblioteca**: no basta con tener los libros. Hay que clasificarlos por tema, ponerles una etiqueta que los describa y ordenarlos en estantes para encontrarlos rápido. Eso es sistematizar.

#### Sistematizar no es recolectar ni analizar

| | Recolectar (EV01) | Sistematizar (EV02) | Analizar (EV03) |
|---|---|---|---|
| **Qué haces** | Reúnes información legal y autorizada | Limpias, ordenas y segmentas lo que reuniste | Calculas, comparas y graficas |
| **Ejemplo** | Descargas el CSV de clientes | Quitas repetidos, unificas formatos y separas clientes de productos | Calculas ventas por ciudad y haces un gráfico |
| **Producto** | Carpeta + matriz | Carpeta 07_sistematizado_xxx + registro de depuración | Plan de análisis, tabla dinámica, dashboard |

#### Por qué sistematizar (según la guía)
| Beneficio | Qué significa | Ejemplo con la empresa |
|---|---|---|
| **Evita pasar por alto información relevante** | Todo queda ordenado y a la vista. | Un archivo de proveedores olvidado en otra carpeta ya no se pierde. |
| **Facilita el análisis** | Datos limpios y en tablas se analizan rápido. | Con la ciudad escrita igual, contar ventas por ciudad toma un minuto. |
| **Facilita la comunicación entre los interesados** | Todos hablan de los mismos datos. | Calidad y ventas usan el mismo listado de clientes. |
| **Favorece la transparencia** | Se sabe quién cambió qué y por qué. | El registro de depuración muestra cada cambio. |
| **Favorece los consensos** | Las partes acuerdan reglas comunes. | Todas las áreas escriben el teléfono con 10 dígitos. |

### 3.2. El ciclo de vida del dato: dónde cae la depuración
Un dato pasa por etapas, como un producto en una fábrica de jugos: llega la fruta (recolección), se guarda en frío (almacenamiento), se lava y se descartan las malas (depuración), se exprime y se mide (análisis) y se envasa y se vende (publicación).

| Etapa | Qué pasa con el dato | Evidencia |
|---|---|---|
| 1. Recolección | Se descarga el archivo de clientes | EV01 |
| 2. Guardado | Se guarda en 03_Datos_crudos de Drive, con respaldo | EV01 |
| **3. Depuración** | **Se quitan repetidos, se unifican formatos y se tratan vacíos** | **EV02 (hoy)** |
| 4. Análisis | Se calculan indicadores y se hacen tablas y gráficos dinámicos | EV03 |
| 5. Publicación y uso | Se comparte el dashboard y se toman decisiones | EV03 en adelante |

> [!verde] **Idea clave:** la depuración va **antes** del análisis. Saltarse esa etapa es la causa más común de resultados equivocados.

### 3.3. Calidad de los datos: seis preguntas para revisar cualquier tabla
Para saber si un dato está «limpio» usamos seis preguntas. Cada una es una **dimensión de calidad**. Es como la **revisión técnico-mecánica** de un carro: se revisan frenos, luces y llantas; si falla una, no pasa.

| Dimensión | La pregunta | Ejemplo |
|---|---|---|
| **Completitud** | ¿Están todos los datos? | Un cliente sin teléfono o sin correo. |
| **Exactitud** | ¿El dato es correcto? | La ciudad dice «Calii», o el precio de una referencia es $200 y debería ser $2.000. |
| **Consistencia** | ¿Se escribe igual en todas partes? | «Cali», «cali», «CALI» y «Santiago de Cali» para la misma ciudad. |
| **Unicidad** | ¿Cada cosa aparece una sola vez? | Pedro Díaz aparece dos veces con la misma factura. |
| **Validez** | ¿Cumple el formato y las reglas? | Un correo sin dominio (`luis.gomez@mail`) o unidades vendidas de `-3`. |
| **Oportunidad** | ¿El dato está actualizado? | El teléfono de un cliente es de 2018 y ya cambió de número. |

**Cómo usarlas:** cuando revises tus datos, recorre las seis preguntas una por una. Cada problema que encuentres cae en una de ellas. Un mismo dato puede fallar en más de una dimensión.

### 3.4. Segmentar con criterios normalizados
La guía pide depurar «según los criterios de segmentación normalizados como políticas organizacionales». Veamos las palabras difíciles:

| Idea | Qué significa | Ejemplo |
|---|---|---|
| **Segmentar** | Dividir los datos en grupos con la misma estructura, según de qué hablan. | El archivo de clientes y ventas se separa en dos tablas: clientes y productos. |
| **Criterios normalizados** | Reglas fijas sobre cómo se escribe y organiza cada campo. | «El teléfono se escribe con 10 dígitos, sin espacios». |
| **Política organizacional** | Esas reglas son decisión de la organización y todas las áreas las aplican. | Ventas y calidad escriben la ciudad igual. |

La guía da dos ejemplos de segmentos:
- **Datos de cliente:** ID, nombres, apellidos, teléfono, correo electrónico, ciudad. Una fila por **persona**.
- **Datos de producto:** referencia, factura de venta, unidades vendidas, ciudad. Una fila por **venta**.

Es como el **archivador de una oficina**: un cajón para facturas, otro para contratos, otro para hojas de vida. Cada cajón tiene su propia ficha con los mismos campos.

> [!tech] **Para pensar:** si Ventas escribe la ciudad «Cali» y Despachos escribe «CALI», ¿qué pasa cuando juntas los dos archivos? Aparecen como ciudades distintas. Por eso la regla se decide una vez y la usan todos.

---

## 4. Tu plantilla de Excel y cómo se aplica una fórmula

### 4.1. La plantilla: un libro, siete hojas
Descarga `Plantilla_EV02_Depuracion.xlsx` desde el Hub (carpeta **Sesión 2**). Con ella practicas en vivo y la reutilizas para entregar tu evidencia.

| Hoja | Para qué sirve | Se usa en |
|---|---|---|
| **LEEME** | Instrucciones, paso a paso y errores frecuentes | Antes de empezar |
| **1_Crudo** | Los 24 clientes tal como llegaron. **No se toca** (está protegida). | Sección 5 |
| **2_Trabajo** | Copia donde depuras: fórmulas, duplicados, vacíos, formatos | Sección 5 |
| **3_Equivalencias** | Tabla «como viene / como debe quedar» para estandarizar ciudades y lista de ciudades válidas | Sección 5 |
| **4_Criterios** | Las reglas de segmentación, listas para ajustar | Sección 6 |
| **5_Clientes** | Segmento de datos de cliente depurados (tabla de Excel) | Sección 6 |
| **6_Producto** | Segmento de datos de producto (tabla de Excel) | Sección 6 |
| **7_Registro** | El registro de depuración: una fila por problema y acción | Sección 6 |

### 4.2. Un archivo por grupo: original y copia
La plantilla **original** nunca se trabaja: se guarda tal cual en `03_Datos_crudos` como prueba de cómo llegaron los datos. El equipo trabaja en **una copia**.

1. **Guarda el original:** el coordinador descarga la plantilla y la sube, **sin editarla**, a la carpeta `03_Datos_crudos` de Drive del equipo (la misma de la EV01).
2. **Haz una copia:** en Drive, clic derecho sobre la plantilla ▸ *Hacer una copia*. Crea la subcarpeta `07_sistematizado_xxx` (clic derecho ▸ *Nueva carpeta*), mueve la copia allí y cámbiale el nombre a `sistematizado_clientes.xlsx`.
3. **Todos trabajan en esa copia.** No hagan una copia por integrante: así el registro y los datos no se contradicen. Para editar **al mismo tiempo**, ábranla con *Hojas de cálculo de Google* (clic derecho ▸ *Abrir con*). Si prefieren Excel de escritorio, trabajen **por turnos**: una persona descarga, edita, vuelve a subir y avisa al equipo.
4. **Repartan el trabajo.** Por ejemplo: una persona normaliza texto y teléfonos, otra ciudades y fechas, otra duplicados y vacíos, otra atípicos y registro. Cada quien anota lo que hace en `7_Registro`.

> [!naranja] **Dos cuidados:** (1) trabaja siempre en `2_Trabajo`; si algo sale mal, copias de nuevo desde `1_Crudo`. (2) Antes de terminar, revisa *Archivo ▸ Historial de versiones* y confirma que están los últimos cambios.

### 4.3. Cómo se aplica CUALQUIER fórmula (léelo primero)
Casi todos los arreglos de la sección 5 usan una fórmula. Se aplican siempre igual:

1. **Columna auxiliar.** Escribe la fórmula en una columna libre a la derecha de los datos (por ejemplo la **L**), nunca encima de la columna original.
2. **Formato General.** Esa columna debe estar en formato **General** (*Inicio ▸ Número ▸ General*). Si está en **Texto**, la fórmula se ve escrita en vez de calcularse. Ojo: al insertar una columna junto a Teléfono, hereda el formato Texto.
3. **Escribe la fórmula en la fila 2.** Haz clic en `L2`, escribe la fórmula (con **punto y coma** entre los argumentos) y pulsa Enter. Verifica que el resultado de esa primera fila sea el correcto.
4. **Llena hacia abajo.** Doble clic en la esquina inferior derecha de `L2` (el cuadrito verde). La referencia cambia sola en cada fila (F2, F3, F4…).
5. **Revisa.** No debe haber errores (`#N/A`, `#¡VALOR!`, `#¿NOMBRE?`).
6. **Pega como valores.** Selecciona la columna L ▸ *Copiar* ▸ haz clic en la primera celda de la columna original ▸ clic derecho ▸ *Pegar valores*. Así reemplazas el dato por el resultado, sin fórmulas.
7. **Borra la columna auxiliar** y anota en `7_Registro` lo que hiciste.

> [!tech] **Dos detalles para que las fórmulas te funcionen.** Si tu Excel separa los argumentos con **coma** en vez de punto y coma, cambia `;` por `,`. Y si tu Excel está en **inglés**, usa los nombres de la tabla siguiente.

| En español | En inglés | Para qué sirve |
|---|---|---|
| `ESPACIOS` | `TRIM` | Quita los espacios de sobra |
| `NOMPROPIO` | `PROPER` | Primera letra de cada palabra en mayúscula |
| `MAYUSC` / `MINUSC` | `UPPER` / `LOWER` | Todo en mayúsculas / minúsculas |
| `SUSTITUIR` | `SUBSTITUTE` | Cambia un texto por otro dentro de una celda |
| `DERECHA` | `RIGHT` | Se queda con los últimos caracteres |
| `FECHANUMERO` | `DATEVALUE` | Convierte un texto en fecha real |
| `BUSCARV` | `VLOOKUP` | Busca un valor en una tabla y trae otro dato |
| `CONTAR.SI` | `COUNTIF` | Cuenta cuántas veces aparece un valor |
| `CONTAR.BLANCO` | `COUNTBLANK` | Cuenta las celdas vacías de un rango |

### 4.4. Errores frecuentes con las fórmulas
| Lo que ves | Por qué pasa | Qué hacer |
|---|---|---|
| **La fórmula aparece escrita, no calculada** | La celda está en formato Texto | Cámbiala a General, borra el contenido y vuelve a escribir la fórmula |
| **`#¿NOMBRE?`** | Excel no reconoce el nombre de la función | Revisa que esté bien escrita en español y que las comillas sean rectas ("), no curvas |
| **Error de sintaxis** | Tu Excel separa argumentos con coma | Cambia `;` por `,` |
| **`#N/A` en BUSCARV** | El valor buscado no está en la tabla | Agrégalo en una fila nueva de `3_Equivalencias` |
| **`#¡VALOR!` en FECHANUMERO** | Excel no reconoce esa fecha | Reescríbela a mano, por ejemplo 7/10/2026 |

---

## 5. Depurar en Excel: cinco problemas y su arreglo
Trabaja con la plantilla abierta, en la hoja **2_Trabajo**. Esta tabla es tu **chuleta**:

| Si ves esto… | Es un problema de… | Herramienta de Excel |
|---|---|---|
| Filas repetidas | Unicidad | *Datos ▸ Quitar duplicados* · `CONTAR.SI` |
| Celdas vacías | Completitud | *Ir a especial ▸ Celdas en blanco* · `CONTAR.BLANCO` |
| Espacios de sobra | Consistencia | `ESPACIOS` |
| Mayúsculas y minúsculas mezcladas | Consistencia | `NOMPROPIO` · `MAYUSC` · `MINUSC` |
| Teléfonos y fechas en formatos distintos | Validez | `SUSTITUIR` · `DERECHA` · `FECHANUMERO` · *Formato de celdas* |
| El mismo valor escrito de varias formas | Consistencia | *Buscar y reemplazar* · `BUSCARV` · tabla de equivalencias |
| Valores raros o imposibles | Exactitud y validez | *Formato condicional* · *Ordenar y filtrar* |
| Que el error no vuelva a pasar | Todas | *Datos ▸ Validación de datos* (lista desplegable) |

> [!verde] **Orden recomendado:** primero se **normaliza** el formato (texto, teléfonos, fechas, ciudades) y **después** se buscan los duplicados. Así Excel reconoce como iguales los registros que lo son.

### 5.1. Texto: espacios y mayúsculas (nombres y apellidos)
**El problema:** «ana maría», «Ana María » y «ANA MARÍA» son tres textos distintos para Excel.

| Original | Fórmula | Resultado |
|---|---|---|
| ana maría | `=NOMPROPIO(ESPACIOS(B2))` | Ana María |
| PÉREZ | `=NOMPROPIO(ESPACIOS(C2))` | Pérez |
|  Díaz  | `=NOMPROPIO(ESPACIOS(C8))` | Díaz |

**Cómo hacerlo**
1. En `L2` escribe `=NOMPROPIO(ESPACIOS(B2))` y llena hacia abajo.
2. Copia la columna L y pégala como **valores** sobre la columna B (Nombres).
3. Repite con `=NOMPROPIO(ESPACIOS(C2))` para la columna C (Apellidos).
4. Anota en el registro: «Nombres y apellidos: ESPACIOS + NOMPROPIO en 24 filas».

**Cómo sabes que quedó bien:** todos los nombres empiezan con mayúscula y no tienen espacios al inicio ni al final.

### 5.2. Teléfonos: un solo formato
**El problema:** hay teléfonos como `3105551234`, `310 555 1234`, `+57 320 555 1111` y `318-555-4321`. **La regla:** 10 dígitos, sin espacios, guiones ni prefijo.

**Cómo hacerlo**
1. En `L2` escribe esta fórmula (selecciona el recuadro y cópiala):

```text title="📞 Fórmula para unificar teléfonos" btn="Copiar fórmula"
=DERECHA(SUSTITUIR(SUSTITUIR(SUSTITUIR(D2;" ";"");"-";"");"+";"");10)
```
2. Llena hacia abajo y pega como valores sobre la columna D.

**Qué hace:** `SUSTITUIR` quita los espacios, los guiones y el signo `+`; `DERECHA(…;10)` se queda con los **últimos 10 dígitos** y elimina el `57`.

**Cómo sabes que quedó bien:** todos los teléfonos tienen 10 dígitos seguidos. Los teléfonos vacíos se tratan en la sección 5.6.

### 5.3. Fechas: un solo formato (año-mes-día)
**El problema:** las fechas están guardadas como **texto** y vienen mezcladas: `05/10/2026`, `7 oct 2026` y `2026-10-06`. Se nota porque se alinean a la **izquierda**. *Formato de celdas* no cambia un texto: primero hay que convertirlo en fecha real.

**Cómo hacerlo**
1. En `L2`, en una columna en formato **General**, escribe `=FECHANUMERO(J2)` y llena hacia abajo. Los textos se vuelven números de fecha.
2. Selecciona la columna L ▸ clic derecho ▸ *Formato de celdas* ▸ *Personalizado* ▸ escribe `yyyy-mm-dd`. Las fechas se ven como `2026-10-05`.
3. Copia la columna L y pégala como **valores** sobre la columna J.
4. Si alguna fila da `#¡VALOR!`, reescribe esa fecha a mano (por ejemplo `7/10/2026`) y vuelve a aplicar la fórmula.

> [!naranja] **El código del año depende del idioma de tu Excel.** Si `yyyy-mm-dd` no te funciona o el resultado sale raro (por ejemplo, aparece el día de la semana), prueba `aaaa-mm-dd`.

**Cómo sabes que quedó bien:** todas las fechas se alinean a la **derecha** y tienen el formato `2026-10-05`.

### 5.4. Ciudades: el mismo valor escrito de varias formas
**El problema:** «Cali», «cali», «CALI», «Calii» y «Santiago de Cali» son la misma ciudad. Un conteo por ciudad las trata como cinco.

**Cómo hacerlo**
1. Mira los valores distintos: activa el filtro (*Ctrl+Mayús+L*) y abre la lista de la columna Ciudad.
2. Decide cómo debe escribirse cada ciudad (la política de la organización). En la hoja **3_Equivalencias** ya están las ciudades de la plantilla: columna A «como viene», columna B «como debe quedar».
3. En `L2` escribe la fórmula y llena hacia abajo:

```text title="🏙️ Fórmula para estandarizar ciudades" btn="Copiar fórmula"
=BUSCARV(F2;'3_Equivalencias'!A:B;2;FALSO)
```
4. Revisa y pega como valores sobre la columna F.

**Qué hace:** toma la ciudad de F2, la busca en la columna A de la hoja `3_Equivalencias` («como viene») y devuelve lo que está en la columna B («como debe quedar»). Usa `FALSO` para buscar el valor exacto. `BUSCARV` **no distingue mayúsculas**: «cali» y «CALI» ya se resuelven con la fila «Cali».

**Si sale `#N/A`:** esa ciudad escrita no está en la columna A. Agrégala en una fila nueva (como viene, como debe quedar) y la fórmula se actualiza sola. Si hay espacios de sobra, usa `=BUSCARV(ESPACIOS(F2);'3_Equivalencias'!A:B;2;FALSO)`.

**Para que no vuelva a pasar:** en la columna Ciudad aplica *Datos ▸ Validación de datos ▸ Lista* con las ciudades válidas. Excel solo dejará escoger de una lista desplegable (en `5_Clientes` y `6_Producto` ya viene hecho).

**Cómo sabes que quedó bien:** en el filtro de Ciudad solo aparecen Cali, Palmira, Yumbo y Jamundí.

### 5.5. Duplicados: filas repetidas
**El problema:** el mismo registro aparece más de una vez e infla los conteos. En la plantilla hay **5 filas duplicadas** (24 filas → 19 clientes).

**Cómo hacerlo**
1. Primero normaliza texto, teléfonos y ciudades (secciones 5.1 a 5.4). Así Excel reconoce como iguales los registros que lo son.
2. **Decide qué columnas definen «el mismo registro».** El **ID no sirve**: cambia entre filas repetidas. Usa **Nombres, Apellidos y Factura**.
3. Selecciona los datos de `2_Trabajo` ▸ *Datos ▸ Quitar duplicados* ▸ marca solo esas columnas ▸ *Aceptar*.
4. Excel avisa cuántas filas quitó. **Anótalo en el registro:** «24 filas antes, 19 después, 5 duplicados».

> [!naranja] **Cuidado:** Excel borra las filas **sin preguntar**. Por eso se trabaja sobre una copia y se anota cuántas se quitaron. Si dos filas «casi» iguales tienen datos distintos, **conserva la más completa**. Por ejemplo, de Pedro Díaz se conserva la fila que tiene correo.

**Cómo sabes que quedó bien:** ya no hay dos filas con el mismo nombre, apellido y factura, y quedaron 19 filas.

### 5.6. Vacíos: celdas sin dato
**El problema:** un vacío puede significar que el dato no existe, que no se capturó o que se perdió. Cada caso se trata distinto.

| Qué decides | Cuándo | Ejemplo |
|---|---|---|
| **Completar** | Hay una fuente confiable para obtener el dato | El correo de Pedro estaba en su otra fila repetida |
| **Marcar** (`SIN DATO` o `POR VERIFICAR`) | No se puede completar, pero el campo es útil | Marta no tiene teléfono → `SIN DATO`. El correo de Luis está incompleto → `POR VERIFICAR` |
| **Excluir la fila** | Le faltan los campos obligatorios y no sirve | Una factura sin referencia ni unidades |
| **Dejar vacío** | El campo es opcional y no se necesita | Segundo teléfono |

**Cómo hacerlo**
1. Selecciona la columna ▸ *Inicio ▸ Buscar y seleccionar ▸ Ir a especial ▸ Celdas en blanco ▸ Aceptar*. Excel resalta todas las vacías.
2. Cuéntalas con `=CONTAR.BLANCO(D2:D25)`.
3. Decide con la tabla de arriba y revisa en la hoja `4_Criterios` si el campo es obligatorio.
4. Con las celdas en blanco seleccionadas, escribe `SIN DATO` (o `POR VERIFICAR` si el dato está incompleto) y pulsa **Ctrl+Enter**: se llenan todas a la vez.
5. Anótalo en el registro.

> [!naranja] **Nunca inventes un dato** para llenar un vacío. Si no tienes la fuente, márcalo y anótalo. Un vacío puede parecer un olvido: «SIN DATO» dice que lo revisaste.

### 5.7. Atípicos: valores raros o imposibles
**El problema:** un atípico es un dato muy distinto a los demás. A veces es un error y a veces una venta excepcional. En la columna Unidades de la plantilla las ventas normales están entre 4 y 12 unidades, pero hay **500, 650, −3 y 0**.

**Cómo hacerlo**
1. Ordena la columna de menor a mayor (*Datos ▸ Ordenar*): los extremos quedan arriba y abajo.
2. Resáltalos: selecciona la columna Unidades ▸ *Inicio ▸ Formato condicional ▸ Resaltar reglas de celdas ▸ Mayor que…* ▸ `100`. Repite con *Menor que…* ▸ `1` (así marca el 0 y los negativos).
3. **Verifica contra la fuente** (la factura o quien capturó el dato). No decidas por intuición.
4. Decide y anota la decisión en el registro:

| Qué encontraste | Qué haces | Ejemplo |
|---|---|---|
| Un **error de digitación** comprobado | Corriges y lo anotas | 500 → 50 (la factura decía 50) |
| Un valor **real pero extremo** | Lo dejas y lo anotas | Un cliente mayorista compró 650 |
| Algo **imposible** que no puedes comprobar | Lo marcas `POR VERIFICAR` | Unidades = −3 sin explicación |

> [!naranja] **Nunca borres un atípico sin registrar** por qué lo hiciste. Un valor extremo puede ser justo lo más interesante de tus datos.

**Cómo sabes que quedó bien:** cada valor resaltado tiene una decisión anotada en el registro.

---

## 6. Segmentar y controlar

### 6.1. Escribe las reglas: la hoja de criterios
Antes de depurar, escribe las reglas: una tabla donde cada fila es un campo y cada columna dice cómo debe escribirse. La plantilla trae la hoja **4_Criterios** con estas reglas; ajústalas a tu caso.

| Campo | Segmento | Tipo | Regla de formato | Obligatorio | Ejemplo válido | Ejemplo inválido |
|---|---|---|---|---|---|---|
| ID | Cliente | Texto | Letra C, guion y 4 dígitos. Único. | Sí | C-0012 | 12 |
| Nombres | Cliente | Texto | Nombre propio, sin espacios de sobra | Sí | Ana María | ana maría |
| Apellidos | Cliente | Texto | Nombre propio, sin espacios de sobra | Sí | Pérez | PÉREZ |
| Teléfono | Cliente | Texto | 10 dígitos, sin espacios ni prefijo | No | 3105551234 | +57 310 555 1234 |
| Correo | Cliente | Texto | Minúsculas, con @ y dominio completo | No | ana.perez@mail.com | luis.gomez@mail |
| Ciudad | Cliente y producto | Lista | Nombre del municipio de la lista oficial | Sí | Cali | CALI |
| Referencia | Producto | Texto | LV- y 3 dígitos | Sí | LV-001 | lv1 |
| Factura | Producto | Texto | F- y 4 dígitos | Sí | F-1001 | 1001 |
| Unidades | Producto | Número entero | Mayor que 0 | Sí | 12 | -3 |
| Fecha | Producto | Fecha | Año-mes-día (2026-10-05) | Sí | 2026-10-05 | 5 oct 2026 |

**¿De dónde salen las reglas?** (1) De los documentos de la empresa (política de tratamiento de datos, manuales, procedimientos). (2) De estándares oficiales (nombres de municipios del DANE, formato de fecha ISO año-mes-día). (3) De una propuesta del equipo cuando no hay reglas: escriben sus criterios y explican por qué los eligieron.

> [!verde] **Primero las reglas, después la depuración.** Sin reglas no sabes qué arreglar; con ellas, cada decisión tiene justificación.

### 6.2. Segmenta: de una tabla mezclada a dos tablas ordenadas
Los datos de `2_Trabajo` mezclan clientes y ventas. Segmentar es separarlos en dos tablas, cada una con su estructura.

1. **Usa las hojas que ya trae la plantilla:** `5_Clientes` y `6_Producto`.
2. **Clientes:** copia de una vez las columnas **A a F** de `2_Trabajo` (ID, Nombres, Apellidos, Teléfono, Correo, Ciudad) y pégalas como valores en `5_Clientes`.
3. **Producto:** copia las columnas **G a J** (Referencia, Factura, Unidades, Fecha) y pégalas como valores en `6_Producto`. Después, **aparte**, copia la columna Ciudad (F) a la última columna de `6_Producto`. El orden de las dos hojas coincide con el de `2_Trabajo` para que pegues sin reordenar.
4. **Asegúrate de que no queden duplicados** (hazlo después de quitar duplicados en `2_Trabajo`).
5. **Aprovecha el formato de tabla:** `5_Clientes` y `6_Producto` ya son tablas de Excel. Una tabla es la forma de «tratar los datos de forma estructurada» que pide la guía. La columna Ciudad solo acepta las ciudades de la lista y Unidades solo enteros mayores que 0.

**Así quedan las primeras filas de `5_Clientes`:**

| ID | Nombres | Apellidos | Teléfono | Correo | Ciudad |
|---|---|---|---|---|---|
| C-0001 | Ana María | Pérez | 3105551234 | ana.perez@mail.com | Cali |
| C-0002 | Luis | Gómez | 3105559876 | POR VERIFICAR | Cali |
| C-0003 | Marta | Rojas | SIN DATO | marta.rojas@mail.com | Cali |
| C-0004 | Pedro | Díaz | 3205551111 | pedro.diaz@mail.com | Palmira |
| C-0005 | Juana | Ríos | 3205552222 | juana.rios@mail.com | Cali |

**Y las primeras filas de `6_Producto`:**

| Referencia | Factura | Unidades | Fecha | Ciudad |
|---|---|---|---|---|
| LV-001 | F-1001 | 12 | 2026-10-05 | Cali |
| LV-002 | F-1002 | 8 | 2026-10-06 | Cali |
| LV-003 | F-1003 | 5 | 2026-10-07 | Cali |
| LV-001 | F-1004 | 50 | 2026-10-08 | Palmira |
| LV-002 | F-1005 | 7 | 2026-10-09 | Cali |

> [!verde] Una buena tabla tiene **una fila por cada cosa y una columna por cada característica**. Si cumples eso, el análisis de la EV03 será mucho más fácil.

### 6.3. El protocolo de trabajo del equipo
La guía dice cómo se sistematiza. Lo convertimos en cuatro pasos:

1. **Define el objeto, los criterios y el protocolo.** ¿Qué vas a sistematizar? El archivo de clientes y ventas. ¿Con qué criterios? La hoja de criterios. ¿Bajo qué protocolo? Trabajar sobre copia, anotar cada cambio, no borrar sin registrar.
2. **Crea un instrumento de control y seguimiento.** Una hoja de cálculo (o Trello o Miro) donde se anota qué se le hizo a cada archivo. Es el registro de depuración. Todos lo pueden consultar en cualquier momento.
3. **Al terminar cada actividad, sincroniza.** Cada integrante, al terminar su parte, actualiza el registro y avisa al equipo qué tocó y dónde quedó. Así nadie repite el trabajo de otro (reprocesos costosos y demorados).
4. **Deja espacio para mejorar el proceso.** Si descubren una regla nueva, actualizan la hoja de criterios y lo anotan.

| Rol en el equipo | Qué hace en la EV02 |
|---|---|
| **Coordinador** | Reparte el trabajo, vigila el cronograma y hace la entrega en Zajuna |
| **Responsable de depuración** | Aplica los arreglos de Excel a los datos |
| **Responsable de segmentación** | Escribe la hoja de criterios y separa los datos en tablas |
| **Responsable del registro de control** | Mantiene el registro de depuración y la carpeta `07_sistematizado_xxx` |

> [!tech] **Si trabajas solo:** un aprendiz puede cumplir los cuatro roles. Lo importante es que el registro refleje todo lo que hiciste.

### 6.4. El registro de depuración (archivo de control)
Es el segundo producto que pide la evidencia: un archivo donde anotas **cada cosa que le hiciste a los datos**. Es como la **bitácora de un piloto** o la historia clínica de un paciente: cada revisión queda anotada con fecha, qué se encontró y qué se hizo. La guía permite hoja de cálculo, Trello u otro; haremos el registro en **Excel**, en la hoja `7_Registro`.

| Columna | Para qué sirve |
|---|---|
| **N.º** | Número de la fila |
| **ID matriz** | Conecta la fila con la **matriz de recolección** de la EV01 (`04_Matriz_de_recoleccion.xlsx`). Si el archivo no está en tu matriz, déjalo vacío. |
| **Archivo de origen / Hoja resultado** | De dónde salió el dato y en qué hoja quedó |
| **Fecha y responsable** | Cuándo y quién lo hizo |
| **Problema detectado** | Qué estaba mal |
| **Acción aplicada** | Qué hiciste |
| **Herramienta** | Con qué lo hiciste (otra persona puede repetirlo) |
| **Filas antes y después** | Permite comprobar el efecto: 24 filas → 19 filas |
| **Estado** | Hecho, En proceso o Pendiente de verificar (lista desplegable) |

**Así se ve un registro de ejemplo:**

| N.º | Origen | Hoja resultado | Responsable | Problema detectado | Acción aplicada | Herramienta | Filas antes | Filas después | Estado |
|---|---|---|---|---|---|---|---|---|---|
| 1 | 1_Crudo | 5_Clientes | Marta | Espacios y mayúsculas mezcladas en nombres y apellidos | Unificar nombres y apellidos | ESPACIOS + NOMPROPIO | 24 | 24 | Hecho |
| 2 | 1_Crudo | 5_Clientes | Marta | Teléfonos en 5 formatos distintos | Dejar 10 dígitos sin espacios ni prefijo | SUSTITUIR + DERECHA | 24 | 24 | Hecho |
| 3 | 1_Crudo | 5_Clientes | Luis | 5 filas duplicadas | Quitar duplicados (conservar la más completa) | Datos ▸ Quitar duplicados | 24 | 19 | Hecho |
| 4 | 1_Crudo | 5_Clientes | Luis | Ciudad escrita de varias formas | Unificar con la tabla de equivalencias | Equivalencias + BUSCARV | 19 | 19 | Hecho |
| 5 | 1_Crudo | 5_Clientes | Ana | Teléfonos vacíos y correos vacíos o incompletos | Marcar SIN DATO y POR VERIFICAR | Ir a especial ▸ Celdas en blanco | 19 | 19 | Pendiente de verificar |
| 6 | 1_Crudo | 6_Producto | Ana | Unidades atípicas: 500, 650, −3 y 0 | Verificar cada factura y decidir; marcar las que no se puedan comprobar | Formato condicional | 19 | 19 | Hecho |

> [!naranja] **Los problemas y las decisiones del ejemplo son ilustrativos.** Tu registro debe reflejar lo que **tu equipo** encontró y decidió. Si un archivo no tiene duplicados, anótalo: «no se encontraron duplicados».

### 6.5. La carpeta 07_sistematizado_xxx: dónde queda todo
La guía pide guardar la información sistematizada en una subcarpeta. Así queda dentro de la carpeta que ya tienes de la EV01:

```text title="📁 Carpeta del equipo después de la EV02" btn="Copiar árbol"
EV01_Recoleccion_[Empresa]_Equipo[N]/        (la misma carpeta de la EV01)
├── 00_LEEME.txt
├── 00_Gestion_del_equipo/
├── 01_Empresa_y_contexto/
├── 02_Sistemas_de_gestion/
├── 03_Datos_crudos/                  (NO se toca: aquí queda la plantilla ORIGINAL)
│   └── Plantilla_EV02_Depuracion.xlsx
├── 04_Matriz_de_recoleccion.xlsx
├── 05_Soportes_legales/
├── 06_Registro_de_depuracion.xlsx    (NUEVO · archivo de control)
└── 07_sistematizado_[xxx]/              (NUEVO · datos depurados)
    └── sistematizado_clientes.xlsx   (la COPIA de la plantilla, ya trabajada)
```

> [!tech] **¿Por qué el 07?** La carpeta lleva número para que quede en orden después de lo de la EV01 (00 a 05) y del registro de la EV02 (06). En la EV03 sigue `08_analisis_xxx`. Conserva la palabra «sistematizado_» después del número, como pide la guía.

| Elemento | Qué va dentro | Detalle |
|---|---|---|
| `03_Datos_crudos/Plantilla_EV02_Depuracion.xlsx` | La **plantilla original**, tal como se descargó | No se abre para trabajar: es la prueba de cómo llegaron los datos |
| `07_sistematizado_[xxx]/` | La subcarpeta de los datos depurados | **xxx** es solo un marcador: la carpeta debe empezar por «07_sistematizado_» y terminar con una palabra corta que diga de qué son los datos. Para esta sesión: `07_sistematizado_LacteosDelValle` (sin espacios ni tildes) |
| `sistematizado_clientes.xlsx` | La **copia** de la plantilla con todo el trabajo hecho | Un solo archivo por grupo |
| `06_Registro_de_depuracion.xlsx` | El archivo de control | Va en la carpeta raíz, junto a la matriz de recolección de la EV01 |

#### Cómo sacar el registro de control de la plantilla
La guía pide el registro como **archivo aparte**. Cuando el registro esté completo:
1. En la plantilla, clic derecho sobre la pestaña `7_Registro` ▸ *Mover o copiar…*
2. En «Al libro», escoge **(nuevo libro)** y marca *Crear una copia*. Aceptar.
3. Guarda el libro nuevo como `06_Registro_de_depuracion.xlsx` y súbelo a la **carpeta raíz** de Drive.

> [!naranja] Haz la copia al **final**, cuando el registro ya esté completo. Si la haces antes y sigues editando la hoja de la plantilla, el archivo de la raíz queda desactualizado.

> [!tech] **No muevas ni borres nada de la EV01.** Trabaja en la misma carpeta de Drive y agrega lo nuevo. Quien abra tu carpeta debe poder comparar en un minuto lo crudo (`03_Datos_crudos`) con lo depurado (`07_sistematizado_xxx`) y leer en el registro qué cambió.

---

## 7. La evidencia EV02 explicada frase por frase
Ya tienes los conceptos y las herramientas. Lee ahora lo que pide la guía y fíjate cómo cada frase corresponde a algo que ya viste.

| Lo que dice la guía | Qué significa | Ejemplo |
|---|---|---|
| *«Se desarrollará a partir de los datos recolectados en la evidencia anterior»* | Trabajan con un conjunto de datos de clientes. Para esta evidencia todos los grupos usan el mismo. | La hoja `1_Crudo` de la plantilla (24 clientes) |
| *«Seleccionando un programa adecuado, versátil y amigable (Excel, Access, Power BI)»* | Escoges la herramienta. En esta sesión trabajamos con **Excel**. | La plantilla de Excel del equipo |
| *«Realice una depuración de los datos»* | Aplicas los arreglos: duplicados, vacíos, formatos, valores distintos y atípicos. | 24 filas → 19 clientes |
| *«Según los criterios de segmentación normalizados como políticas organizacionales»* | Defines reglas para cada campo y las aplicas. | La hoja `4_Criterios` |
| *«Guarde la información sistematizada en una subcarpeta: sistematizado_xxx»* | Los datos depurados van en una subcarpeta con ese nombre. | `07_sistematizado_LacteosDelValle` |
| *«Datos de cliente (…) · Datos producto (…)»* | Son ejemplos de segmentos: cada uno con sus campos. | Hojas `5_Clientes` y `6_Producto` |
| *«Instrumento de control y seguimiento»* | Un registro de lo que se hizo, consultable por todos. | `06_Registro_de_depuracion.xlsx` |
| **Producto:** carpeta en la nube + archivo de control | Carpeta clasificada en subcarpetas (máx. **10 GB**) y archivo de registro (máx. **1 GB**). | Drive y un Excel |
| *«Envío en el espacio GA5-220501114-AA1-EV02»* | Entregas en Zajuna, igual que la EV01. | PDF con portada, introducción y enlace |

**Lo que la sistematización debe lograr (según la guía):** clasificar la información de acuerdo con lineamientos organizacionales, caracterizarla según las necesidades de la organización y tratar los datos de forma estructurada si es posible.

---

## 8. Paso a paso para construir la EV02
Estos son los nueve pasos del equipo, en orden. Sigue el orden para no repetir trabajo.

### Paso 1: Reúnanse y repartan el trabajo
**Qué debes hacer:** descargar la plantilla, subirla a Drive y repartir los roles (sección 6.3).
**Cómo sabes que quedó bien:** cada integrante sabe qué parte hace y dónde anota lo que hace.

### Paso 2: Guarden el original y trabajen en una copia
**Qué debes hacer:** subir la plantilla original a `03_Datos_crudos` sin editarla y hacer una copia en `07_sistematizado_xxx` llamada `sistematizado_clientes.xlsx` (sección 4.2).
**Cómo sabes que quedó bien:** hay un archivo original intacto y una copia de trabajo.

### Paso 3: Escriban la hoja de criterios
**Qué debes hacer:** revisar y ajustar `4_Criterios`: una fila por campo, con regla, si es obligatorio y ejemplos válido e inválido (sección 6.1).
**Cómo sabes que quedó bien:** cada campo tiene una regla clara y dos ejemplos.

### Paso 4: Depuren con las herramientas de Excel
**Qué debes hacer:** en `2_Trabajo`, aplicar en este orden: nombres y apellidos, teléfonos, fechas, ciudades, duplicados, vacíos y atípicos (sección 5). Anotar cada paso.
**Cómo sabes que quedó bien:** los datos cumplen las reglas de la hoja de criterios y quedan 19 filas.

### Paso 5: Segmenten en tablas
**Qué debes hacer:** pasar los datos depurados a `5_Clientes` y `6_Producto` (sección 6.2).
**Cómo sabes que quedó bien:** dos tablas, una fila por persona y una fila por venta, sin duplicados.

### Paso 6: Llenen el registro de depuración
**Qué debes hacer:** una fila por cada problema detectado y cada acción aplicada en `7_Registro` (sección 6.4).
**Cómo sabes que quedó bien:** los números del registro coinciden con los de las tablas (24 → 19).

### Paso 7: Guarden todo en la carpeta de Drive
**Qué debes hacer:** dejar la copia en `07_sistematizado_xxx` y sacar el registro como `06_Registro_de_depuracion.xlsx` en la carpeta raíz (sección 6.5).
**Cómo sabes que quedó bien:** la carpeta tiene la estructura de la sección 6.5.

### Paso 8: Revisen con el checklist y sincronicen
**Qué debes hacer:** recorrer la lista de chequeo (sección 15) y verificar que el registro y las tablas coincidan.
**Cómo sabes que quedó bien:** todas las casillas marcadas.

### Paso 9: Compartan, armen el PDF y entreguen
**Qué debes hacer:** compartir la carpeta con **instructorjuliantrujilo@gmail.com** (permiso *Comentador*), probar el enlace en una ventana de incógnito, armar el PDF de entrega (sección 10) y subirlo a Zajuna.
**Cómo sabes que quedó bien:** el enlace abre sin iniciar sesión y el PDF está subido antes de la fecha límite.

---

## 9. Ejemplo resuelto: una EV02 de principio a fin
> [!naranja] **Aviso:** la empresa **«Lácteos del Valle S.A.S.» es ficticia**. Sus 24 clientes son los datos con los que trabajan todos los grupos.

| Paso | Qué hizo el equipo del ejemplo |
|---|---|
| 1. Datos de partida | Plantilla original guardada en `03_Datos_crudos`: hoja `1_Crudo` con 24 filas y 10 columnas de clientes y ventas |
| 2. Copia de trabajo | Hicieron una copia en `07_sistematizado_xxx` (`sistematizado_clientes.xlsx`) y trabajaron en `2_Trabajo`. El original no se tocó |
| 3. Criterios | Revisaron la hoja `4_Criterios` con los campos de cliente y de producto (la ciudad es de ambos) |
| 4. Formatos | `NOMPROPIO(ESPACIOS())` en nombres y apellidos; teléfonos a 10 dígitos; fechas a año-mes-día |
| 5. Duplicados | Quitaron 5 filas repetidas. Quedaron 19 clientes |
| 6. Ciudades | Las variantes de Cali, Palmira y Jamundí se unificaron con la hoja `3_Equivalencias` |
| 7. Vacíos | Teléfonos sin dato → `SIN DATO`. Correos incompletos → `POR VERIFICAR`. El correo de Pedro se completó con su fila repetida |
| 8. Atípicos | Revisaron 500, 650, −3 y 0 en Unidades: corrigieron los errores comprobables y marcaron los demás |
| 9. Segmentación | Dos tablas: hoja `5_Clientes` (19 filas) y hoja `6_Producto` (19 ventas) |
| 10. Registro y entrega | Registro con 6 acciones. Libro en Drive y PDF `EV02_NombreEmpresa.pdf` subido a Zajuna |

**Resultado:** son **24 filas que se vuelven 19 clientes confiables**, y cada cambio quedó explicado en el registro. Eso es sistematizar.

---

## 10. El PDF de entrega: portada, introducción y enlace
En Zajuna **no se sube la carpeta**: se sube **un PDF** que la presenta. Es igual que en la EV01; cambian el número de evidencia y la introducción.

1. **Abre un documento nuevo** (o una copia del de la EV01) en Google Docs o Word. Usa letra legible (Arial o Calibri 11–12).
2. **Copia la plantilla** de abajo y reemplaza todo lo que está entre [corchetes].
3. **Escribe la introducción** (5 a 8 renglones): con qué datos trabajaron, qué problemas encontraron, qué hicieron y cómo quedó el resultado.
4. **Pega el enlace de la carpeta** y haz clic en él para comprobar que abre. La carpeta debe estar compartida con **instructorjuliantrujilo@gmail.com** (*Comentador*).
5. **Descarga el PDF:** en Google Docs, *Archivo ▸ Descargar ▸ Documento PDF*; en Word, *Archivo ▸ Guardar como ▸ PDF*.
6. **Nómbralo `EV02_NombreEmpresa.pdf`**, donde NombreEmpresa es la **empresa que eligió tu equipo en la EV01**, sin tildes, espacios ni símbolos. Por ejemplo `EV02_LacteosDelValle.pdf`.
7. **Súbelo a Zajuna**, en el espacio *GA5-220501114-AA1-EV02*, antes del miércoles, 11 de noviembre de 2026, 11:59 p. m. Un integrante lo sube por todo el equipo.

```text title="📄 Plantilla de portada, introducción y enlace" btn="Copiar plantilla"
SERVICIO NACIONAL DE APRENDIZAJE – SENA
Tecnólogo en Gestión del Desarrollo Administrativo e Innovación
Ficha: [3466323 o 3466324]

EVIDENCIA GA5-220501114-AA1-EV02
Sistematización de datos recopilados

EMPRESA DE LA EV01: [nombre de la empresa que eligió tu equipo]

INTEGRANTES (si trabajas solo, deja una sola fila)
1. [Nombre completo] – C.C. [documento] – Rol: [coordinador]
2. [Nombre completo] – C.C. [documento] – Rol: [responsable de depuración]
3. [Nombre completo] – C.C. [documento] – Rol: [responsable de segmentación]
4. [Nombre completo] – C.C. [documento] – Rol: [responsable del registro de control]

Instructor: Julián Andrés Trujillo Morales
Fecha de entrega: [día de mes de año]
------------------------------------------------------------
INTRODUCCIÓN
Escribe de 5 a 8 renglones: con qué datos trabajaron (la plantilla de clientes de Lácteos del Valle),
qué problemas encontraron, qué hicieron y cómo quedó el resultado.
------------------------------------------------------------
CARPETA DE DRIVE CON LA EVIDENCIA
Enlace: [pegar enlace]
Compartida con instructorjuliantrujilo@gmail.com (permiso Comentador)

QUÉ HAY DE NUEVO EN LA CARPETA
- 07_sistematizado_[xxx]/: la copia de la plantilla ya trabajada (sistematizado_clientes.xlsx)
- 06_Registro_de_depuracion.xlsx: el archivo de control
- 03_Datos_crudos/Plantilla_EV02_Depuracion.xlsx: la plantilla original sin cambios
```

> [!naranja] Los nombres de **todos los integrantes** van dentro de la portada, no en el nombre del archivo. Si trabajas solo, deja una sola fila en la tabla de integrantes.

---

## 11. Cómo se evalúa la evidencia y cómo dejarlo evidenciado
El instrumento de evaluación **IE-GA5-220501114-AA1-EV02** tiene cuatro grupos de indicadores. Así dejas evidenciado cada uno:

| Indicador del instrumento | Cómo lo dejas evidenciado |
|---|---|
| **Aplica los protocolos de sistematización sugeridos** | Trabajaste sobre copia, anotaste cada cambio y llevaste el registro. Hoja de criterios incluida. |
| **Sistematiza según los protocolos normativos y legales** | Los datos de la plantilla son ficticios y no contienen datos personales reales. Trabajas sobre copia y no divulgas datos de personas. |
| **Evidencia la sistematización según los requerimientos de la organización** | La hoja `4_Criterios` define cómo debe quedar cada campo (la política de datos de la organización) y los datos están segmentados y estructurados. |
| **Entrega en el formato sugerido** | Carpeta con subcarpeta `07_sistematizado_xxx` y archivo de registro; PDF con portada y enlace. |
| **Usa la web y la nube** para almacenar en carpetas y subcarpetas | Todo en Drive, con la estructura de la EV01 más lo nuevo. |
| **Entrega en el plazo esperado** | Antes del miércoles, 11 de noviembre de 2026, 11:59 p. m. |

Los **criterios de evaluación del RAP** son los mismos de toda la actividad: reconocer las fuentes de información según normativa, describir los componentes de modelos matemáticos y estadísticos, analizar actividades cotidianas con técnicas de toma de decisiones, determinar los elementos de la ciencia de los datos, reconocer las técnicas de análisis de datos y reconocer herramientas tecnológicas para el ciclo de vida, la gestión y el análisis de datos de acuerdo con la normativa.

---

## 12. Errores frecuentes y cómo evitarlos
| Error | Por qué es un problema | Cómo evitarlo |
|---|---|---|
| **Trabajar sobre la plantilla original** | Pierdes la prueba de cómo llegaron los datos | Guardar el original en `03_Datos_crudos` y trabajar en una copia |
| **Quitar duplicados antes de normalizar** | Excel no ve como iguales «ana maría» y «Ana María » | Normalizar texto, teléfonos y ciudades primero |
| **Usar el ID para buscar duplicados** | El ID cambia entre filas repetidas y no detecta nada | Marcar Nombres, Apellidos y Factura |
| **Escribir la fórmula en una celda con formato Texto** | La fórmula se muestra escrita y no se calcula | Usar una columna auxiliar en formato General |
| **Inventar datos para llenar vacíos** | Falsea la información | Marcar `SIN DATO` o `POR VERIFICAR` |
| **Borrar atípicos sin registrar** | Se pierde información y no hay transparencia | Verificar, decidir y anotar en el registro |
| **Depurar sin anotar** | La evidencia del protocolo no existe | Una fila en el registro por cada acción |
| **Hacer análisis (promedios, gráficos)** | Es de la EV03 y no se pide | Dejar los datos limpios y documentados |
| **Copiar el registro antes de terminarlo** | El archivo de la raíz queda desactualizado | Hacer la copia al final |
| **Entregar un enlace que pide iniciar sesión** | El evaluador no puede abrirlo | Probar el enlace en ventana de incógnito |

---

## 13. Preguntas frecuentes
**¿Por qué todos usamos los mismos clientes?** Porque muchas empresas no publican los datos de sus clientes. Los 24 clientes de la plantilla son ficticios y el proceso de sistematización es el mismo que con datos reales.

**¿Los clientes de la plantilla son personas reales?** No. Son datos ficticios creados para practicar; por eso se pueden usar sin pedir autorización.

**¿Tengo que usar Power Query o Access?** No. La guía permite Excel, Access o Power BI. Excel es suficiente. *Power Query* (*Datos ▸ Obtener y transformar*) hace estos arreglos con clics y guarda los pasos; es opcional.

**¿Cuántos problemas tengo que encontrar?** Los que realmente tengan tus datos. Si un archivo no tiene duplicados, anótalo en el registro: «no se encontraron duplicados».

**¿Puedo trabajar solo?** Sí. Un aprendiz puede cumplir los cuatro roles y entrega el mismo PDF (con una sola fila de integrantes).

**¿Puedo cambiar lo que entregué en la EV01?** No cambies la carpeta de datos crudos ni la matriz. Solo agrega lo nuevo.

**¿Todos los integrantes deben subir algo a Zajuna?** No. Un integrante sube el PDF por todo el equipo; los nombres de todos van en la portada.

**¿Por qué el registro va en un archivo aparte si ya está en la plantilla?** Porque la guía pide un **archivo de registro** para el control de depuración. Se llena dentro de la plantilla mientras trabajan y, al terminar, se copia a `06_Registro_de_depuracion.xlsx`.

---

## 14. Plan de trabajo sugerido
Esta es una **sugerencia** de reparto del tiempo para llegar con calma a la fecha límite:

| Cuándo | Qué hacer | Resultado |
|---|---|---|
| Martes 3 – miércoles 4 de noviembre | Entregar la **EV01** (4 de noviembre). Descargar la plantilla y subirla a la carpeta de Drive del equipo. | EV01 entregada y plantilla en Drive |
| Jueves 5 de noviembre | Escribir y ajustar la hoja de criterios | Criterios definidos |
| Viernes 6 – domingo 8 de noviembre | Depurar y segmentar. Llevar el registro mientras trabajan. | Datos depurados |
| Lunes 9 de noviembre | Revisar con el checklist y armar el PDF | PDF listo |
| Martes 10 de noviembre (Sesión 3) | Resolver dudas y pasar a la EV03 | Observaciones |
| Miércoles 11 de noviembre | **Entregar en Zajuna** (mejor un día antes) | EV02 entregada |

> [!tech] **Consejo:** no dejen la entrega para el último minuto. Si el enlace falla o falta un archivo, necesitarán tiempo para corregirlo. Entreguen **un día antes** si pueden.

---

## 15. Lista de chequeo anti-rechazo
Marca cada casilla antes de subir tu evidencia a Zajuna:

- [ ] La plantilla original está en `03_Datos_crudos` sin modificar — Y la hoja 1_Crudo de tu copia no se tocó.
- [ ] Hay hoja de criterios — Cada campo tiene regla y ejemplos válido e inválido.
- [ ] Aplicaste los arreglos — Duplicados, vacíos, formatos, valores escritos distinto y atípicos.
- [ ] Los datos están segmentados y en tablas — Una tabla por segmento con formato de tabla de Excel.
- [ ] El registro está completo — Una fila por cada problema con acción, herramienta, filas antes y después.
- [ ] Los números coinciden — Las filas del registro coinciden con las de las tablas (24 → 19).
- [ ] La subcarpeta `07_sistematizado_xxx` está en la carpeta de la EV01 — Con la copia de la plantilla como sistematizado_clientes.xlsx.
- [ ] `06_Registro_de_depuracion.xlsx` está en la carpeta raíz — Copia final de la hoja 7_Registro.
- [ ] La carpeta está compartida con el instructor — Permiso Comentador a instructorjuliantrujilo@gmail.com.
- [ ] El enlace abre sin iniciar sesión — Probado desde una ventana de incógnito.
- [ ] El PDF de entrega está listo — Portada con ficha, empresa y todos los integrantes; introducción; enlace; nombre EV02_NombreEmpresa.pdf.

---

## 16. Glosario
| Término | Significado |
|---|---|
| **Sistematizar** | Dejar la información ordenada, limpia y organizada con reglas para que se pueda usar |
| **Depurar** | Limpiar los datos: quitar repetidos, corregir errores y unificar formatos |
| **Segmentar** | Dividir los datos en grupos con la misma estructura |
| **Criterio normalizado** | Regla fija sobre cómo se escribe y organiza un campo |
| **Política organizacional** | Decisión de la organización que todas las áreas aplican |
| **Duplicado** | El mismo registro escrito más de una vez |
| **Vacío (nulo)** | Celda sin dato |
| **Atípico** | Valor muy distinto a los demás |
| **Dato crudo** | Dato tal como llegó, sin modificar |
| **Registro de depuración** | Archivo donde se anota qué se le hizo a cada dato |
| **Columna auxiliar** | Columna temporal donde se escribe una fórmula antes de pegar los valores |
| **Tabla de Excel** | Rango con formato de tabla (*Ctrl+T*) que estructura los datos |
| **Calidad de datos** | Qué tan confiable es un dato: completitud, exactitud, consistencia, unicidad, validez y oportunidad |

---

## 17. Referencias
- Guía de aprendizaje 5 — Competencia 220501114, actividad GA5-220501114-AA1 (disponible en el Hub).
- Instrumento de evaluación IE-GA5-220501114-AA1-EV02 — Sistematización de datos recopilados.
- Presentación de la Sesión 2 y plantilla de Excel `Plantilla_EV02_Depuracion.xlsx` (disponibles en el Hub).
- Microsoft. *Ayuda de Excel*: Quitar duplicados, Validación de datos y Formato condicional.

---

*Manual didáctico para los aprendices de la Ficha 3466323 y 3466324 — Gestión del Desarrollo Administrativo e Innovación. Instructor: Julián Andrés Trujillo Morales.*
