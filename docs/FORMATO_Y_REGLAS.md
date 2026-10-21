# Formato de los archivos y reglas de traducción

Antes de editar cualquier archivo, lee esto. El juego es sensible al formato y un error pequeño
puede cerrarlo.

## Formato de los archivos `*_US.bin`

- Texto UTF-8 **sin BOM**.
- Cada fila termina con un retorno de carro (`\r`, CR). No hay saltos de línea `\n` en ningún archivo.
- Los campos de una fila se separan con `|`.
- Dentro de un campo, `†` es un salto de línea del texto.
- Cada archivo traducido tiene el **mismo número de filas y de campos** que el original en inglés.
- En listas y menús separados con `†` (por ejemplo las opciones de un menú), conserva el mismo número de `†`
  que el original. En textos largos (diálogos de NPC, descripciones, textos de tienda, descripciones de
  títulos) las líneas se reacomodaron para que quepan en el recuadro, así que el número de `†` puede ser
  distinto al del original. Si cambias un texto largo, reacomoda las líneas con el mismo criterio.
- Códigos de formato (`%d`, `%s`, `%.2f`, `%%`, etc.): iguales y en el mismo orden que en el original.
  Evita escribir `%` seguido de un espacio y una letra (por ejemplo `% s` o `% n`), porque el juego
  podría leerlo como un código. Escribe "5%, según" en lugar de "5% según".

Cuidado con los editores: muchos convierten los saltos de línea al guardar. Usa un editor que respete CR
(o un script que lea y escriba en modo binario) y no guardes con saltos `\n` ni `\r\n`.

## Nombres que funcionan como clave

El nombre de un objeto aparece en varios archivos y el juego los relaciona por el texto exacto. Por ejemplo, los objetos de
`EventShop_US.bin` (lo que cuesta y lo que se recibe) deben escribirse **igual** que en `Item_Info_US.bin`. Si cambias el nombre de
un objeto, cámbialo en todos los archivos donde aparece.

## Caracteres

El juego solo dibuja bien tildes, ñ, ¿ y ¡ en estos textos:

- `NpcDialogWindow`, `ExceptrNpcDialogWindow`, `QuestDialog` y `Quiz_Event`.
- 11 filas de `TextAttach` (ids 1335 a 1339, 1401 a 1405 y 1421).

En todo lo demás se usa ASCII, sin tildes, y la ñ se escribe "nh" (por ejemplo "danho").

## Límites de espacio

Medidos dentro del juego. Si un texto es más largo, se sale o se corta.

| Ventana o elemento | Límite aproximado |
| --- | --- |
| Diálogo de NPC con marco | 37 caracteres por línea como máximo (con 38 se corta); mejor 35 |
| Diálogo de NPC sin marco | 50 caracteres por línea y unas 15 líneas (17 menos el número de opciones) |
| Placa con el nombre del NPC | 18 a 20 caracteres |
| Botones pequeños (Aceptar, etc.) | 6 a 7 caracteres, alineados a la izquierda |
| Botones de la ventana del Tamer | 9 a 10 caracteres |
| Nombre de habilidad | 26 caracteres angostos |
| Descripción de título de Tamer | 22 caracteres por línea |
| Descripciones (`Comment`) | 56 a 57 caracteres por línea |
| Desplegables de zona (reclutamiento de grupo) | 19 caracteres |
| Cuadro emergente de las características de la Enciclopedia (`Ec_Attribute`, `Ec_Battle_Attribute`) | 6 líneas de unos 30 caracteres (unos 170 en total); lo que pase de ahí se corta al final |

**Tamaño máximo por campo.** Parece haber un límite de unos 10 KB (10 240 bytes) por campo. Un
mensaje de `TextAttach` (id 2809, una lista larga de textos de combate) creció de 9 790 a 10 254 bytes
en una revisión de la traducción y, con ella, el juego se cerraba al hablar en el chat del Gremio.
Al acortarlo a 9 451 bytes dejó de pasar. Mantén cada campo por debajo del tamaño del original.

## Glosario

| Inglés | Español |
| --- | --- |
| Tamer | Tamer (no se traduce) |
| Nombres de Digimon | No se traducen |
| Baby | Bebé |
| Rookie | Novato |
| Champion | Campeón |
| Ultimate | Ultra |
| Mega | Mega |
| Virus Buster | Cazavirus |
| Royal Knights | Caballeros Reales |
| X-Antibody | Anticuerpo X |
| Guild | Gremio |
| Leave Guild (botón) | Abandonar |
| Inventory | Bolsa |
| Debuff | debuff |
| Card Slash | Card Slash |
| Billion (Bits) | Billón (1,000,000,000) |
| Darkness Dungeon | Mazmorra de la Oscuridad |
| DigiXros | DigiXros |
| ATK / DEF | ATA / DEF |
| HP / VP | PS / PM |
| STR / INT / AGI / CON | FUE / INT / AGI / CON |
| EVP | EVP |
| Battle Rating | Puntuación de batalla |

## Abreviaturas en nombres de mapas

Los nombres de zona aparecen en desplegables angostos, así que se abrevian:

- Pisos: `P1`, `P2`, `P3`. Sótanos: `S1`, `S2`.
- `Maz.` = Mazmorra.
- Puntos cardinales: `N.`, `S.`, `E.`, `O.`.

Estos mismos nombres se usan donde el juego muestra una ubicación: `Map_US.bin`, `Dex_US.bin` (columna
"Lugar donde aparece"), `Tamer_Title_US.bin` ("Cómo obtener"), `Riddle_US.bin` y las líneas "Ubicacion:" de
`NPC_Function_US.bin`. Si cambias un nombre en un lugar, cámbialo en todos. En diálogos y descripciones
largas se pueden usar los nombres completos.

## Cómo probar un cambio

1. Copia el archivo modificado a la carpeta `Language` del juego (con la copia de seguridad hecha).
2. Reinicia el juego y abre la ventana donde sale el texto.
3. Si algo se sale del recuadro, acórtalo y vuelve a probar.
