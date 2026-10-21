# Resumen del trabajo realizado

Esta es la lista de lo que incluye la traducción y de cómo se revisó. Sirve para saber qué esperar de cada archivo
y para no repetir trabajo si quieres colaborar.

## Qué se tradujo

Los 43 archivos `*_US.bin` de la carpeta `Language`, agrupados por tema:

| Tema | Archivos |
| --- | --- |
| Objetos, materiales y colecciones | `Item_Info`, `Collection`, `MakeItem` |
| Tiendas del juego y de eventos | `InGameShop_*` (7 archivos), `EventShop`, `P_Shop`, `ShopDialog`, `ShopIconName` |
| Enciclopedia y Digimon | `Digimon`, `Dex`, `Comment`, `M_Comment` (frases de los Digimon en combate), `MonsterRegen`, `Card_Info` |
| Habilidades y características | `Digimon_Skill`, `Attribute`, `Add_Attribute`, `Ec_Attribute`, `Ec_Battle_Attribute`, `E_Attribute_Text`, `BuffOriginalData`, `M_Pattern_Message`, `Resonance` |
| NPC, misiones y diálogos | `NPC_INFO`, `NPC_Function`, `NpcDialogWindow`, `ExceptrNpcDialogWindow`, `QuestDialog`, `Quiz_Event`, `TutorialWindow`, `Pop-UpWindow` |
| Acertijos | `Riddle` |
| Mapas y títulos | `Map`, `Tamer_Title`, `Digimon_Title` |
| Interfaz y mensajes del sistema | `TextAttach`, `SystemMessage` |

## Nombres

- **Digimon:** nombre oficial o del doblaje latino en todos los archivos (nombres unidos, erratas y variantes corregidas).
  Los 12 Devas quedan con sus nombres correctos y las variantes de Antylamon como `Antylamon(Bueno)` y `Antylamon(Malo)`.
  Detalle en [NOMBRES_DIGIMON.md](NOMBRES_DIGIMON.md).
- **Personajes humanos:** nombre del doblaje latino y orden Nombre Apellido. Detalle en [NOMBRES_PERSONAJES.md](NOMBRES_PERSONAJES.md).
- **Habilidades:** revisión completa de las 1061 filas, con 124 nombres reescritos para que suenen naturales y para evitar palabras
  que no son neutras. El mismo nombre se usa en la enciclopedia, el combate, las cartas, los títulos y los acertijos.
  Detalle en [HABILIDADES.md](HABILIDADES.md).
- **Términos del juego:** Novato, Campeón, Cazavirus, Caballeros Reales, Anticuerpo X, Gremio, PS, PM, FUE, EVP… Tabla completa en
  [FORMATO_Y_REGLAS.md](FORMATO_Y_REGLAS.md).
- **Bits:** las cantidades desde mil millones se escriben "billón" en cupones, discos comprimidos, NPC y mensajes del sistema.
- **Nombres de mapa:** abreviados de la misma forma en todas las ventanas (Maz., P1, S1, N., S., E., O.).

## Texto que cabe en los recuadros

- Diálogos de NPC, misiones y quiz de eventos: líneas de 37 caracteres como máximo (con 38 se cortan).
- Enciclopedia (`Comment`): descripciones reajustadas al ancho de la ventana (56 caracteres por línea).
- Tooltips de características: máximo de 6 líneas. Se acortaron los dos que se cortaban (Escudo Sagrado Oscuro (OVER) y Fin de la Paradoja).
- Botones y listas: textos acortados donde el original se desbordaba (por ejemplo "Abandonar" en la ventana del Gremio y en
  Tamer Info, "Ingreso :" en Guild Info, "Dar Patrones" e "Ir por piso" en los NPC de Gallantmon).
- Tamer Info: la lista de colores de Digizoide se lee "Dorado Digizoide", con su espacio.
- Objetos: espacios sobrantes corregidos.

## Revisión completa de

- `Comment` (enciclopedia), `Item_Info`, `Riddle` (todos los bloques) y los diálogos de NPC.
- Consistencia entre archivos: un mismo objeto, Digimon o lugar se llama igual en todas partes, y los nombres de los objetos
  de `EventShop` coinciden con los de `Item_Info`.
- Ortografía y puntuación. Las tildes, la ñ, ¿ y ¡ se usan solo donde el juego las dibuja (ver las reglas).

## Cómo se verifica cada archivo

Antes de publicar se comprueba con un script que cada archivo cumple:

- UTF-8 sin BOM, filas separadas por CR y ningún salto `\n`.
- El mismo número de filas y de campos que el original en inglés.
- Los mismos códigos de formato (`%d`, `%s`…) y en el mismo orden.
- Ningún campo por encima del límite de tamaño y ningún carácter acentuado fuera de los archivos permitidos.
- Ninguna línea de diálogo por encima del ancho máximo.

## Lo que no se puede arreglar desde estos archivos

Ver [Limitaciones conocidas](../README.md#limitaciones-conocidas) en el README: ventanas con texto dentro de imágenes y el nombre de los Digimon
salvajes sobre el mapa y en batalla, que los manda el servidor en inglés.
