# OPERACIÓN AION — BRIEFING PARA COWORK

## QUÉ ES ESTE PROYECTO
Gymkana competitiva para 12 adultos (ingenieros, +30 años) organizada por Aitor Tilla
en Villa Colona. **4 equipos de 3 personas** (Alfa, Beta, Gamma, Delta).
Temática: IA autónoma llamada AION que ha activado el Protocolo Ω.
Formato de carrera pura: primer equipo en introducir su código en el terminal central gana.

---

## ESTRUCTURA DE ARCHIVOS

```
AION/                           ← Raíz del proyecto
  terminal.html                 ← Terminal compartido (pantalla grande)
  presentacion.html             ← Intro robot AION animado

  alfa/                         ← Un servidor por equipo
    p1.html                     ← P1: Nube de símbolos animada
    p2vk3m.html                 ← P2: Audio Morse (Web Audio API)
    p3nw8x.html                 ← P3: Tabla de sensores
    p4rx5q.html                 ← P4: Validación palabra overlay
    p5jt2b.html                 ← P5: Cancelación de señales de color
    p6hs9d.html                 ← P6: Trazado narrativo Dr. Navarro
    p7mf4k.html                 ← P7: Mastermind 5 procesos (tiles de color)
    p8gy7n.html                 ← P8: Intersección de líneas con regla
    p9cw6r.html                 ← P9: Activación en orden (4 nodos)

  beta/                         ← Mismos nombres, contenido diferente
  gamma/
  delta/

  GridP4/                       ← Grids A3 para imprimir y pegar en pared (P4)
```

**Arranque del servidor:**
```
cd AION
python3 -m http.server 8080
```

**URL base:** `http://[IP]:8080/alfa/p1.html`  
P1 es el único archivo sin nombre obfuscado (es la entrada pública por QR del dossier).  
Los archivos p2–p9 tienen nombres aleatorios para impedir acceso directo por URL.

---

## TABLA MAESTRA DE CÓDIGOS

| Prueba | ALFA | BETA | GAMMA | DELTA |
|--------|------|------|-------|-------|
| P1 (nube símbolos) | 879897 | 987978 | 798789 | 987879 |
| P2 (morse audio) | OMEGA | ALERT | ABORT | SIGMA |
| P3 (sensores) | 4851 | 9623 | 7140 | 3076 |
| P4 (overlay) | DARK | MESH | FLUX | LOCK |
| P5 (colores) | 7X03 | 9K21 | 4M08 | 5N29 |
| P6 (trazado) | 5927 | 3814 | 6043 | 2358 |
| P7 (mastermind) | 2619 | 4753 | 8302 | 1485 |
| P8 (intersección) | 7284 | 5391 | 6047 | 3916 |
| P9 auth final | AION-ALFA-2847 | AION-BETA-5193 | AION-GAMMA-6720 | AION-DELTA-4031 |

**Terminal final** — campo CÉLULA acepta: ALFA / BETA / GAMMA / DELTA  
Código por campo (4 dígitos): ALFA=2847, BETA=5193, GAMMA=6720, DELTA=4031

---

## FLUJO DE CADA EQUIPO

```
QR en dossier
  → P1 (nube símbolos, 6 dígitos)
    → pista zona DESCANSO → QR 2
  → P2 (audio Morse, 5 letras) valida aquí mismo
    → pista zona PASEO → QR 3
  → P3 (sensores, 4 dígitos)
    → pista zona CALOR → QR 4
  → P4 FÍSICO (overlay A5 sobre nube A3) → palabra 4 letras
  → P4 HTML (valida palabra)
    → pista zona ÁRBOL → QR 5
  → P5 (cancelación señales de color, 4 chars)
    → pista zona BBQ → QR 6
  → P6 FÍSICO (cuadrícula números) + P6 HTML (narrativa Navarro)
    → 4 dígitos del trazado
    → pista zona BANDERAS → QR 7
  → P7 (Mastermind 5 colores, deducción)
    → revela código cuando se resuelve → enlace directo a P8
  → P8 FÍSICO (nube símbolos + regla) + P8 HTML
    → 4 dígitos de intersecciones → enlace directo a P9 (sin QR)
  → P9 (activación 4 nodos en orden correcto)
    → revela código auth final
  → TERMINAL CENTRAL (selector CÉLULA + código 4 dígitos)
```

**Orden de activación P9** (igual para todos los equipos):
1. INTERFERENCIA → código P8
2. ESPECTRAL → código P5
3. MONITORIZACIÓN → código P3
4. SECUENCIA → código P7

*La pista del orden está al final del texto narrativo de P6.*

---

## UBICACIONES FÍSICAS DE LOS QR
*(Edita esta sección para adaptarla al espacio real)*

Hay 7 QR físicos (P1–P7). P8 enlaza directamente a P9 sin QR adicional.  
Cada prueba tiene 4 QR (uno por equipo) colocados en la misma zona física.

| QR | Accede a | Nombre zona (en HTML) | Texto de pista (en HTML) | Ubicación física |
|----|----------|-----------------------|--------------------------|------------------|
| QR 1 | P1 — SEÑAL | — | QR incluido en el dossier | [DEFINE AQUÍ la ubicación del dossier inicial] |
| QR 2 | P2 — PULSO | DESCANSO | "Ante el portón de la finca, el banquito de granito guarda silencio." | [DEFINE AQUÍ dónde poner el QR 2] |
| QR 3 | P3 — MONITORIZACIÓN | PASEO | "Móntate y pedalea, aunque las ruedas nunca lleguen a ningún lado." | [DEFINE AQUÍ dónde poner el QR 3] |
| QR 4 | P4 — MÁSCARA | CALOR | "En invierno tu gran amigo. La estufa de pellets guarda más que calor." | [DEFINE AQUÍ dónde poner el QR 4] |
| QR 5 | P5 — ESPECTRAL | ÁRBOL | "Gordales, hojiblanca, manzanilla... Mira hacia las ramas del olivo." | [DEFINE AQUÍ dónde poner el QR 5] |
| QR 6 | P6 — TRAZADO | BBQ | "Donde el fuego reúne y el humo asciende. La brasa sabe tu destino." | [DEFINE AQUÍ dónde poner el QR 6] |
| QR 7 | P7 — SECUENCIA | BANDERAS | "Ondean al viento. Europa, Andalucía y más. Sigue los colores." | [DEFINE AQUÍ dónde poner el QR 7] |

**Para cambiar el texto de pista en los HTML:**  
Busca en cada `p[N]*.html` de cada equipo el texto correspondiente y cámbialo.  
El texto de pista está en el mensaje de éxito de cada prueba, dentro de la función JS de validación.

**Para generar los QR:**  
28 QR en total (7 pruebas × 4 equipos). Cada QR apunta a la URL de su equipo:
```
QR 2 ALFA  → http://[IP]:8080/alfa/p2vk3m.html
QR 2 BETA  → http://[IP]:8080/beta/p2vk3m.html
QR 2 GAMMA → http://[IP]:8080/gamma/p2vk3m.html
QR 2 DELTA → http://[IP]:8080/delta/p2vk3m.html
```

---

## SOLUCIONES DETALLADAS

### P1 — Nube de símbolos
6 tipos de símbolo (⬡◆●▲■✦), todos con más de 6 unidades.
Contar cada tipo, introducir de mayor a menor (según tamaño del símbolo en pantalla).

| Equipo | ⬡ | ◆ | ● | ▲ | ■ | ✦ | Código |
|--------|---|---|---|---|---|---|--------|
| ALFA | 8 | 7 | 9 | 8 | 9 | 7 | 879897 |
| BETA | 9 | 8 | 7 | 9 | 7 | 8 | 987978 |
| GAMMA | 7 | 9 | 8 | 7 | 8 | 9 | 798789 |
| DELTA | 9 | 8 | 7 | 8 | 7 | 9 | 987879 |

### P2 — Audio Morse
Escuchan pitidos, descifran con tabla Morse del dossier (Sección 2).
Palabras: OMEGA / ALERT / ABORT / SIGMA (5 letras cada una).
Campo maxlength=5. Velocidad ajustable: `UNIT=0.25` (más rápido) o `UNIT=0.35` (más lento).

### P3 — Sensores en alarma
14 filas desordenadas (LECTURA vs LÍMITE). Alarma = LECTURA > LÍMITE.
El último dígito de LECTURA aparece en **negrita** en los HTML.
Código = último dígito de LECTURA de cada sensor en alarma, en orden de tabla.

- ALFA: S-03(724→**4**), S-07(918→**8**), S-10(485→**5**), S-12(561→**1**) → 4851
- BETA: S-02(859→**9**), S-05(716→**6**), S-08(382→**2**), S-11(623→**3**) → 9623
- GAMMA: S-03(817→**7**), S-06(581→**1**), S-09(374→**4**), S-13(810→**0**) → 7140
- DELTA: S-08(823→**3**), S-12(790→**0**), S-14(617→**7**), S-13(936→**6**) → 3076

### P4 — Overlay físico
Nube A3 pegada en pared (450 caracteres + señuelos).
Plantilla A5 con 4 ventanas circulares para recortar.
4 marcas de alineación (⊕⊗⊖⊙) posicionadas con precisión.
Al colocar correctamente → ventanas revelan 4 letras de la palabra.

### P5 — Cancelación de señales de color
4 operaciones. Cada círculo muestra nombre de color de señal (OLIVA, NARANJA, GRANATE, OCRE, etc.) y su color visual.
Identificar primarios de cada señal con la tabla del dossier, cancelar el compartido, buscar resultado.

- ALFA: 7X03
- BETA: 9K21
- GAMMA: 4M08
- DELTA: 5N29

### P6 — Trazado Dr. Navarro
Cuadrícula 10×10 de números (cols A-J, filas 1-10, arriba a abajo).
Narrativa en HTML con direcciones cardinales (Norte/Sur/Este/Oeste). Sin leyenda.
Las 4 paradas en negrita → valor de esa casilla → código.

- ALFA: inicio G-7 mirando Norte → E4=5, B8=9, H6=2, D2=7 → 5927
- BETA: inicio E-2 mirando Oeste → C5=3, G3=8, A9=1, F7=4 → 3814
- GAMMA: inicio H-3 mirando Sur → H8=6, C6=0, J3=4, F9=3 → 6043
- DELTA: inicio F-2 mirando Sur → C5=2, G3=3, E8=5, H6=8 → 2358

### P7 — Mastermind
5 procesos de colores (KERNEL verde, CIPHER rojo, NEXUS azul, VAULT dorado, GHOST morado).
Verde=posición correcta, Amarillo=desplazado. Código se revela al resolver.

- ALFA: NEXUS→KERNEL→GHOST→VAULT→CIPHER → 2619
- BETA: VAULT→CIPHER→KERNEL→GHOST→NEXUS → 4753
- GAMMA: GHOST→NEXUS→CIPHER→KERNEL→VAULT → 8302
- DELTA: CIPHER→VAULT→NEXUS→GHOST→KERNEL → 1485

### P8 — Intersección de líneas
Hoja A5 con 8 pares de símbolos (⊕★◆▲⊗✦❖▼).
El HTML muestra los pares con notación SÍM² para indicar que cada símbolo aparece dos veces.
Trazar 8 líneas con regla. El número en la intersección física = dígito.

- ALFA: ⊕∩★=7, ◆∩▲=2, ⊗∩✦=8, ❖∩▼=4 → 7284
- BETA: ⊕∩★=5, ◆∩▲=3, ⊗∩✦=9, ❖∩▼=1 → 5391
- GAMMA: ⊕∩★=6, ◆∩▲=0, ⊗∩✦=4, ❖∩▼=7 → 6047
- DELTA: ⊕∩★=3, ◆∩▲=9, ⊗∩✦=1, ❖∩▼=6 → 3916

### P9 — Activación de nodos
4 nodos deben activarse en orden fijo introduciendo el código de cada uno.
Error en cualquier paso = reinicio completo al nodo 1.

Orden: INTERFERENCIA (P8) → ESPECTRAL (P5) → MONITORIZACIÓN (P3) → SECUENCIA (P7)

| Nodo | Prueba | ALFA | BETA | GAMMA | DELTA |
|------|--------|------|------|-------|-------|
| INTERFERENCIA | P8 | 7284 | 5391 | 6047 | 3916 |
| ESPECTRAL | P5 | 7X03 | 9K21 | 4M08 | 5N29 |
| MONITORIZACIÓN | P3 | 4851 | 9623 | 7140 | 3076 |
| SECUENCIA | P7 | 2619 | 4753 | 8302 | 1485 |

Al completar los 4 nodos → muestra el código de autorización final:  
AION-ALFA-2847 / AION-BETA-5193 / AION-GAMMA-6720 / AION-DELTA-4031

---

## ESTILO Y DISEÑO

- **Tema HTML**: fondo blanco, textos verde oscuro (#006644 para ALFA)
- **Fuente**: Courier New (monoespaciada, todo el juego)
- **Terminal**: fondo oscuro (dramático), selector CÉLULA + campo código 4 dígitos

| Equipo | Color primario | Uso |
|--------|---------------|-----|
| ALFA | #006644 (verde) | Textos, bordes |
| BETA | #003388 (azul) | Textos, bordes |
| GAMMA | #550088 (morado) | Textos, bordes |
| DELTA | #884400 (naranja) | Textos, bordes |

---

## PENDIENTES ANTES DEL EVENTO

- [ ] **Definir ubicaciones físicas de QR** — completar la tabla de la sección "UBICACIONES FÍSICAS DE LOS QR"
- [ ] **Generar los 28 QR** cuando se conozca la IP del servidor (`python3 -m http.server 8080`)
- [ ] **Probar tiempo real** de la gymkana (estimado 90–120 min)
- [ ] **Ajustar velocidad audio Morse** si hace falta (parámetro `UNIT=0.25` en p2vk3m.html)
- [ ] **Verificar que P4 overlay encaja** físicamente con grid A3 al imprimir al 100%

---

## DATOS TÉCNICOS

- **Servidor local**: `python3 -m http.server 8080` en carpeta AION/
- **URLs**: `http://[IP]:8080/[equipo]/[archivo]` — p.ej. `http://192.168.1.100:8080/alfa/p1.html`
- **Todos los móviles en la misma red WiFi**
- **Terminal**: abrir `terminal.html` en dispositivo central/proyectado
- **Presentación**: abrir `presentacion.html` antes del juego
