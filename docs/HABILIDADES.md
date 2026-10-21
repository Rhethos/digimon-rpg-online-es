# Revision de nombres de habilidades (Digimon_Skill_US.bin)

Revision completa de las 1061 filas. Los nombres se aplicaron de forma identica en
Digimon_Skill, Dex, Digimon, Comment (descripciones), Riddle, TextAttach, Card_Info,
Ec_Attribute / Ec_Battle_Attribute, M_Pattern_Message y Tamer_Title.

## Lo que se pudo confirmar en la red (doblaje latino / wiki en espanol)
| Habilidad (EN) | Nombre confirmado | Fuente |
|---|---|---|
| Air Shot | Disparo de Aire | doblaje latino (Patamon) |
| Magical Fire | Fuego Magico | doblaje latino (Biyomon) |
| Baby Flame | Flama Bebe | doblaje latino (Agumon) |
| Petit Thunder | Mini Trueno | doblaje latino (Tentomon) |
| Blue Thunder | Relampago Azul | doblaje latino (Tentomon; la lista no dice a que ataque japones corresponde, se asigno por nombre) |
| Horn Attack | Ataque de Cuerno | doblaje latino (Gabumon) |
| Beak Pecker | Picotazo | doblaje latino (Biyomon) |
| Cocytus Breath | Aliento de Lobo Metalico | doblaje latino (MetalGarurumon), digimon.fandom.com/es |
| Mega Flame | Megaflama | coherente con el doblaje (Flama Bebe / Mini Trueno) |

Fuentes: digifunclub.webnode.cl/digimons, digimon.fandom.com/es/wiki/MetalGarurumon.
Solo se pudieron leer las paginas de Agumon, Gabumon, Biyomon, Tentomon, Patamon y
MetalGarurumon; el resto de la wiki no abre desde aqui. Todo lo demas son nombres creados.

## Errores corregidos
- Allergy Shower / Rain of Pollen estaban intercambiados: ahora Lluvia de Alergia / Lluvia de Polen.
- Crimson Flare / Crimson Blaze estaban intercambiados: ahora Llamarada Carmesi / Llama Carmesi.
- Scratch Beat seguia como "Golpe de Aranhazos": ahora Zarpazo Ritmico.
- Descripciones (Comment) que todavia traian nombres viejos o con salto de linea en medio del nombre
  (Garra sin Chatarra, Rafaga Dragon, Voltear la Mesa con Furia, Triturador de Estrella Ardiente...): unificadas.
- Card_Info / Riddle / M_Pattern / Tamer_Title con nombres distintos a los de la habilidad
  (Temor Urgente, Ola de Marea, Meteoro Endlich, Ola Oscura, Corriente Mega): unificados.

## Verificacion de nombres viejos
Barrido final de los 43 archivos (sin distinguir tildes/mayusculas ni saltos de linea dentro del nombre) buscando
los 180 nombres anteriores de las habilidades renombradas. Lo que quedaba se corrigio: descripciones de Digimon
(Comment), acertijos, cartas, titulos y los dialogos de Kongoumon y Panjyamon (NpcDialogWindow, "Punho de Hielo").
En las descripciones, "punhetazo(s)" en prosa paso a "golpe(s)" y los nombres propios a "Punho(s)" (Punho Planetario, Punho de 7 Segundos).

## Cambios de redaccion (124 nombres)
- **"Punhetazo" fuera**: podia leerse como una palabra vulgar en portugues. Ahora "Punho ..." (Punho de Hielo, Punho Neko, Megapunho...).
- **Doble antes del sustantivo**: Doble Fuego, Doble Burbuja, Doble Filo, Doble Impacto, Doble Sonico.
- **Petit / Little / Pico -> Mini** (y sin "nh"): Mini Fuego, Mini Trueno, Mini Torbellino, Mini Picotazo, Mini Cuerno, Mini Dardos.
- **Mega / Giga coherentes**: Megaflama, Megablaster, Megamuerte, Gigamuerte, Gigablaster, Gigadestructor.
- **Conectores que faltaban** (sonaban a traduccion literal): Fuego de Zorro, Cuerno de Escarabajo, Martillo de Cola,
  Aliento de Tundra, Aliento de Fuego, Guantelete de Trueno, Latigo de Espinas, Piedra de Rosetta, Portal del Cenit...
- **Palabras que no son neutras o no existen**: Rodamiento (=cojinete) -> Rodada; Placaje -> Tacleo; Tiovivo -> Carrusel Frenetico;
  Concha (vulgar en el Cono Sur) -> Caracola Giratoria; Plumario/Plumaria -> de Plumas; Pinha -> Cono de Pino; Hilo de Aranha -> Hilo Aracnido;
  Oidos Sonicos -> Orejas Sonicas; Lanza Auricular -> Lanza de Orejas; Hazanha -> Proeza; Dinamitas Sexys -> Dinamitas Sexis.
- **Sentido**: Volcanic Driver (era "Conductor") -> Piledriver Volcanico (llave de lucha libre); Red Reamer -> Barrena Roja;
  Shield Counter -> Contraataque de Escudo; Spitfire -> Escupefuego; Death Behind -> Muerte por la Espalda;
  Omega Blade -> Espada Omega; Water Screw -> Espiral de Agua; Blitz Arm -> Brazo Blitz (igual que Accel Arm del acertijo).
- **Mal acortados por el ancho**: Tormenta Superdim. -> Tormenta Dimensional; Rapto del Dios Muerte -> Rapto Dios de la Muerte;
  Doble Canhon Doble Petalos -> Doble Canhon Floral; Doble Guardia Brazos -> Guardia de Dos Brazos.

## Se dejo igual a proposito
- Nombres japoneses/alemanes/italianos/latinos del original (Tenryuzanha, Schwarz Donner, Quo Vadis, Kyukyoku...): son los nombres reales del ataque.
  Algunos "Kyukyoku ..." son mas anchos que el cuadro del tooltip, pero el original en ingles tambien los muestra asi.
- "Ladrido" (fila 286): el ingles dice "San no Awa" pero el coreano es "ladrido" y es de Labramon.
- Giga Gadiac Raid / Gradiac Raid: no se pudo verificar la ortografia; se respeta la del original.
- "Doble Xros Brave Beat Rock" se ve un poco ancho en el tooltip (igual que en ingles).

## Pendiente de ver en el juego
- Ec_Attribute: nombre "Infierno de Llamas" (mas largo que "Infierno Igneo").
- Tamer_Title (Friolento): ahora "Aliento de Lobo / Metalico" en dos lineas.
