# Digimon RPG Online: traducción al español latino

Traducción al español neutro latinoamericano de los textos del MMO **Digimon RPG Online**.
Son los archivos de idioma `*_US.bin` del juego, ya traducidos: objetos, habilidades, Digimon,
misiones, diálogos de NPC, tiendas, mapas, enciclopedia, acertijos, interfaz y mensajes del sistema.

> Proyecto comunitario. No está afiliado al juego ni a sus propietarios.

> [!IMPORTANT]
> **Después de cada mantenimiento del juego tendrás que volver a copiar los archivos.** Cuando el juego tiene mantenimiento
> restablece la carpeta `Language` a los archivos originales en inglés, y la traducción desaparece hasta que la copies de nuevo.
> Guarda el `.zip` descargado para hacerlo rápido (ver [Después de un mantenimiento](#después-de-un-mantenimiento)).

## Estado

- Versión actual: **v1.0**.
- 43 archivos traducidos y probados dentro del juego.
- Se siguen corrigiendo detalles a medida que se encuentran textos que se salen de los recuadros.
- Hay textos que **no se pueden traducir desde estos archivos** (ver [Limitaciones](#limitaciones-conocidas)).

## Qué incluye

- **Nombres oficiales y latinos.** Digimon con su nombre del doblaje y de las series (por ejemplo Gatomon, Myotismon,
  Gallantmon, Antylamon) y personajes humanos con el nombre y el orden del doblaje latino (Tai Kamiya, Matt Ishida, Kari Kamiya).
  Detalle en [docs/NOMBRES_DIGIMON.md](docs/NOMBRES_DIGIMON.md) y [docs/NOMBRES_PERSONAJES.md](docs/NOMBRES_PERSONAJES.md).
- **Habilidades.** Revisión de las más de mil habilidades: nombres coherentes en la enciclopedia, el combate, las cartas y los acertijos.
  Detalle en [docs/HABILIDADES.md](docs/HABILIDADES.md).
- **Texto que cabe en los recuadros.** Diálogos de NPC y misiones, descripciones de la enciclopedia, botones, tooltips y listas
  se ajustaron al ancho real de cada ventana, para que no se corten.
- **Acertijos, enciclopedia, objetos y tiendas** revisados completos, con los mismos nombres en todas las ventanas.
- **Términos unificados** (Novato, Campeón, Cazavirus, Caballeros Reales, Anticuerpo X, Gremio, PS, PM, FUE…) y cantidades de Bits
  escritas como las usa la comunidad del juego (1 billón = 1,000,000,000).

El resumen completo del trabajo está en [docs/TRABAJO_REALIZADO.md](docs/TRABAJO_REALIZADO.md).

## Cómo instalarla

1. Cierra el juego.
2. Entra a la carpeta de instalación del juego y abre la carpeta `Language`.
3. **Haz una copia de seguridad** de esa carpeta (cópiala en otro lugar). Así puedes volver al inglés cuando quieras.
4. Descarga el último `.zip` desde [Releases](../../releases) y descomprímelo.
5. Copia los archivos `*_US.bin` dentro de la carpeta `Language` del juego, reemplazando los que ya están.
   (En este repositorio también están en la carpeta [`Language/`](Language).)
6. Abre el juego.

Para desinstalar, vuelve a copiar tu copia de seguridad.

### Después de un mantenimiento

Si después de un mantenimiento el juego vuelve a salir en inglés, es normal: se restablecieron los archivos de `Language`.
Cierra el juego, copia otra vez los archivos `*_US.bin` del `.zip` dentro de la carpeta `Language` (paso 5) y ábrelo.
No hace falta repetir la copia de seguridad.

Si el juego se cierra o no abre después de instalarla, restaura la copia de seguridad y abre un
[Issue](../../issues) contando qué pasó, qué estabas haciendo y a qué hora.

## Qué se traduce y qué no

- "Tamer" se queda como está.
- Los nombres de los Digimon no se traducen (se usa su nombre oficial).
- Los nombres de aplicaciones y "Sevens" se quedan como están.
- Las cantidades de Bits desde mil millones se escriben "billón" (1 billón = 1,000,000,000), igual que "billion" en inglés.
- El juego solo muestra bien tildes, ñ, ¿ y ¡ en algunos textos (diálogos de NPC y misiones, por ejemplo).
  En el resto se usa ASCII y la ñ se escribe "nh" (por ejemplo "danho").
- Las reglas completas están en [docs/FORMATO_Y_REGLAS.md](docs/FORMATO_Y_REGLAS.md).

## Limitaciones conocidas

Estos textos salen en inglés porque están dentro de imágenes o los escribe el propio cliente o
el servidor del juego. No están en los archivos de idioma, así que no se pueden cambiar aquí:

- Títulos de ventanas como Duel Application, RECRUIT CREATE, TAMER INFO, PARTNER DIGIMON, LOGIN y GUILD INFO.
- Etiquetas como Guild, Grade, Personnel, Status, Withdrawable Bit, Withdraw, CARD e ITEM.
- Botones como Create y Cancel de algunas ventanas.
- Los nombres de mapa que aparecen después de "En" en la ventana del Tamer y algunos anuncios del servidor.
- El nombre que aparece sobre los Digimon salvajes en el mapa y en batalla (por ejemplo "Andiramon(Vice)") lo manda el servidor y sale en inglés. En la Enciclopedia, las misiones y los diálogos sí aparece el nombre traducido.

Si encuentras otro texto en inglés, puede estar en esta lista o ser un texto que se nos pasó.
Abre un Issue con una captura.

## Cómo reportar un error

Abre un [Issue](../../issues) (hay un formulario que pide estos datos):

- Una **captura de pantalla** donde se vea el problema.
- El nombre de la ventana o el NPC.
- Qué dice el texto y qué debería decir (si lo sabes).

Los problemas más comunes son textos que se salen del recuadro o se cortan, y términos que no suenan bien.

## Cómo colaborar

Lee antes [docs/FORMATO_Y_REGLAS.md](docs/FORMATO_Y_REGLAS.md). Los archivos tienen un formato muy
estricto (separadores, saltos de línea, códigos como `%d` y límites de ancho) y un error pequeño
puede cerrar el juego.

## Aviso

Este repositorio solo contiene archivos de texto de idioma traducidos. No incluye el cliente del juego,
imágenes ni otros archivos del juego. Digimon y los nombres relacionados pertenecen a sus
respectivos propietarios. Si algún titular de derechos pide retirar el contenido, se retirará.
