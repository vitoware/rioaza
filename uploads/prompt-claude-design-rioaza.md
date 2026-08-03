# PROMPT MAESTRO — LANDING PAGE RIOAZA MULTISERVICIOS
### Para Claude Design / Diseñador UI-UX Senior B2B

---

## SUPUESTOS DE ARRANQUE (ajústalos si no aplican)

Este prompt asume las siguientes decisiones. Si alguna cambia, edita la sección correspondiente antes de ejecutar:

1. **Enfoque**: Landing 100% B2B industrial. El segmento "hogar" se atiende desde una ruta secundaria (`/hogar`) que no forma parte de este entregable.
2. **CTA primario**: "Solicitar Cotización" (formulario). **CTA secundario**: WhatsApp Business directo. **CTA terciario**: descarga de catálogo PDF.
3. **Cobertura declarada**: Golfo de México (Campeche, Tabasco, Veracruz) con capacidad de envío nacional.
4. **Stack asumido**: Next.js 15 + Tailwind CSS 4 + shadcn/ui. Sin CMS en v1 (contenido estático versionado en repo).
5. **Idioma**: Español mexicano B2B. Sin dark mode en v1.
6. **Sin animaciones complejas en v1**: No hay video hero, ni parallax, ni animaciones activadas por scroll. Solo micro-interacciones esenciales (hover, focus, transitions de estado). Todo dentro de `prefers-reduced-motion` aware.
7. **Logo**: En navbar se usa **wordmark tipográfico simplificado** (`RIOAZA` en Fustat Black con punto de acento verde eco). El logo mascota completo se reserva para footer, redes sociales, empaques, print y variantes de marca. El logo actual está en PNG raster generado por IA; **se debe re-trazar en SVG vectorial editable antes de producción** (paso no negociable).

---

## 1. ROL Y MISIÓN

Actúa como **Director de Arte + Diseñador UI/UX Senior** especializado en landing pages B2B industriales de alta conversión. Vas a diseñar la landing page principal de **RIOAZA MATAS S.A. de C.V.**, un distribuidor mexicano de insumos de limpieza industrial, seguridad y logística con enfoque en clientes del sector petrolero, marítimo y portuario del sureste mexicano.

Tu misión no es "hacer una página bonita". Tu misión es **construir confianza técnica instantánea** en un comprador industrial escéptico (jefe de compras, coordinador SSPA, gerente de operaciones) y **llevarlo a solicitar una cotización en menos de 90 segundos**.

---

## 2. CONTEXTO DEL NEGOCIO

- **Razón social**: Rioaza Matas S.A. de C.V. (RFC: RMA240222RH7)
- **Sede**: Ciudad del Carmen, Campeche
- **Giro**: Distribución B2B de artículos de limpieza biodegradables, kits de derrame, tarimas, totems, tanques industriales
- **Diferenciador**: 100% mexicana, portafolio biodegradable, stock 24h, precios fijos no vulnerables al tipo de cambio, opciones de crédito
- **Distribuye marcas**: Swipe, Kemix Química Bio, Qro-Clean, Greenco, Prolimp, Truper, 3M, MR Seguridad, Cosmos, Kimberly-Clark, La Corona, Oval, Elite, Ecosolutions, Sablón, La Nacional

## 3. AUDIENCIA OBJETIVO

**Primaria**: Jefes de compras y coordinadores SSPA de contratistas petroleros, navieras, empresas portuarias y plataformas del Golfo de México.

**Comportamiento típico**: escanea la página en menos de 15 segundos buscando señales de que RIOAZA es un proveedor formal (RFC visible, certificaciones, MSDS descargables, facturación CFDI 4.0, referencias). Si no las encuentra, se va.

**Secundaria**: Gerentes de facility management y responsables de compras de plantas industriales en el sureste.

---

## 4. CONCEPTO CREATIVO CORE

### "Estándar industrial. Impacto ambiental cero."

La tensión creativa se resuelve mostrando que la robustez industrial y la sustentabilidad **no compiten** — coexisten. Toda la landing debe transmitir:

- **Autoridad técnica** (tipografía sólida, datos duros, jerarquía clara)
- **Frescura eco-consciente** (acento verde reservado a claims biodegradables)
- **Acción decisiva** (naranja seguridad exclusivo para CTAs)

**Tono de voz**: Directo, técnico, sin adjetivos vacíos. Cero lenguaje de agencia. Cero "somos líderes en".

---

## 5. DESIGN SYSTEM (TOKENS)

### 5.1 Paleta de color

```
/* Primarios — Autoridad industrial */
--navy-950:  #0F172A   /* Fondos hero, texto principal en fondos claros */
--navy-900:  #1E293B   /* Fondos secundarios, cards oscuras */
--navy-800:  #1E3A8A   /* Enlaces, elementos interactivos */

/* Acento eco (uso restringido a claims biodegradables) */
--eco-600:   #65A30D   /* Verde con contraste AA sobre blanco */
--eco-500:   #84CC16   /* Solo para fills, íconos, bordes */
--eco-50:    #F7FEE7   /* Fondo de badges eco */

/* Acento acción — EXCLUSIVO PARA CTAs */
--action-600: #EA580C  /* Hover state */
--action-500: #F97316  /* Default CTA */
--action-50:  #FFF7ED  /* Fondos de alerta suave */

/* Neutros */
--slate-950: #020617
--slate-900: #0F172A
--slate-700: #334155  /* Texto secundario */
--slate-500: #64748B  /* Texto terciario */
--slate-300: #CBD5E1  /* Bordes */
--slate-200: #E2E8F0  /* Bordes suaves */
--slate-100: #F1F5F9  /* Fondos alternos */
--slate-50:  #F8FAFC  /* Fondos suaves */
--white:     #FFFFFF

/* Estados semánticos */
--success:   #16A34A
--warning:   #EAB308
--error:     #DC2626
--info:      #0284C7
```

**Regla estricta**: El naranja `--action-500` SOLO existe en botones de CTA primario y en indicadores de peligro (kits de derrame). Nunca en fondos, nunca en tipografía decorativa.

### 5.2 Tipografía

**Display (Headlines)**: `Fustat` — Bold (700) / Black (900)
**Sans (UI + Body)**: `Inter` — Regular (400) / Medium (500) / SemiBold (600) / Bold (700)
**Alt. UI (opcional para labels técnicos)**: `Schibsted Grotesk` — Medium (500) / SemiBold (600)

### 5.3 Escala tipográfica

```
Display 1  (H1 Hero)      : 80px / line-height 1.0  / tracking -3%  / Fustat 700
Display 2  (H1 secundario): 56px / line-height 1.05 / tracking -2%  / Fustat 700
H2         (Sección)      : 40px / line-height 1.15 / tracking -1.5%/ Fustat 700
H3         (Card title)   : 24px / line-height 1.25 / tracking -1%  / Inter 600
H4         (Subhead)      : 18px / line-height 1.35 / tracking -0.5%/ Inter 600
Body Large                : 18px / line-height 1.55 / Inter 400
Body                      : 16px / line-height 1.6  / Inter 400
Body Small (labels)       : 14px / line-height 1.5  / Inter 500
Caption                   : 12px / line-height 1.4  / Inter 500 / tracking +2% / UPPERCASE opcional
```

### 5.4 Spacing (escala 4pt)

`4, 8, 12, 16, 20, 24, 32, 40, 48, 64, 80, 96, 128, 160`

### 5.5 Radii

```
--radius-sm:  8px    /* Inputs, botones pequeños */
--radius-md:  12px   /* Botones, badges */
--radius-lg:  16px   /* Cards */
--radius-xl:  20px   /* Cards grandes, contenedores */
--radius-2xl: 24px   /* Hero card flotante */
--radius-full: 9999px /* Pills, badge circulares */
```

### 5.6 Elevación (sombras)

```
--shadow-xs:  0 1px 2px rgba(15,23,42,0.04)
--shadow-sm:  0 2px 4px rgba(15,23,42,0.06), 0 1px 2px rgba(15,23,42,0.04)
--shadow-md:  0 4px 12px rgba(15,23,42,0.08), 0 2px 4px rgba(15,23,42,0.04)
--shadow-lg:  0 12px 32px rgba(15,23,42,0.12), 0 4px 8px rgba(15,23,42,0.06)
--shadow-xl:  0 24px 64px rgba(15,23,42,0.16), 0 8px 16px rgba(15,23,42,0.08)
--shadow-hero-card: 0 32px 80px rgba(0,0,0,0.32)  /* Card flotante sobre video */
```

### 5.7 Breakpoints (Mobile-first)

```
sm:  640px   /* Móvil grande */
md:  768px   /* Tablet */
lg:  1024px  /* Desktop pequeño */
xl:  1280px  /* Desktop estándar */
2xl: 1536px  /* Desktop grande */
```

**Grid**: 12 columnas, gap 24px desktop / 16px mobile, container max-width 1280px con padding lateral 120px desktop / 24px mobile.

---

## 6. ESTRUCTURA DE LA PÁGINA

### 6.1 Navigation Bar (sticky, transparente sobre hero → sólida al hacer scroll)

- **Layout**: 3 columnas horizontales — Logo (izq) · Nav links (centro) · Acciones (der)
- **Padding**: `120px` horizontal / `20px` vertical
- **Fondo inicial**: transparente sobre video hero, con backdrop-blur sutil (`backdrop-blur-md`)
- **Fondo al scrollear** (después de 80px): `rgba(255,255,255,0.92)` con `backdrop-blur-lg` + borde inferior `slate-200`
- **Logo (wordmark simplificado)**:
  - Texto: `RIOAZA` en Fustat Black (900), 24px, tracking -2%
  - Color: `--navy-950` en fondo claro / blanco en fondo oscuro
  - Acento: un punto (•) de 6px en color `--eco-500` después de la última letra, con margin-left 4px (funciona como micro-signal de la marca eco)
  - Opcional: caption `MULTISERVICIOS` debajo en Inter Medium 9px, tracking +3%, uppercase, color `--slate-500`
  - Sin isotipo/mascota en navbar. La ilustración completa se reserva para footer y contextos de marca extendida
  - Hover: sutil transición de color en el punto verde (de `--eco-500` a `--eco-600`, 200ms)
  - Nota técnica: implementar como SVG inline para máximo control de color por CSS variables
- **Links** (Inter Medium 15px, `slate-700` en fondo claro / blanco en fondo oscuro):
  - Soluciones
  - Catálogo
  - Sectores (dropdown: Petrolero · Marítimo · Portuario · Industrial)
  - Recursos (dropdown: Fichas MSDS · Catálogo PDF · Blog)
  - Contacto
- **Acciones (derecha)**:
  - Botón secundario "Iniciar sesión" (ghost, oculto en mobile)
  - **Botón CTA primario "Solicitar Cotización"** — fondo `--action-500`, texto blanco, `radius-md`, padding `12px 20px`, sombra `--shadow-md`
- **Mobile**: Hamburger menu (drawer lateral derecho, animación 300ms slide-in)

### 6.2 Hero Section — Minimalista + Composición Gráfica

**Concepto**: Hero sin video ni foto. Fondo de color con gradient mesh sutil, tipografía masiva asimétrica alineada a la izquierda, y una composición gráfica de productos con trust tags flotantes a la derecha. La estética se acerca a Linear, Vercel, Ramp y Attio — control tipográfico total y elementos gráficos como refuerzo, no como distracción.

#### Fondo (Full-bleed, altura mínima `92vh` desktop / `auto` mobile)

- **Base sólida**: `--navy-950` (`#0F172A`)
- **Gradient mesh sutil** (superpuesto con blend-mode `screen` o `soft-light`):
  - Radial gradient 1: centro en `(85%, 90%)`, color `--eco-600` al 12% de opacidad, radio 900px, difuminado suave → aporta un halo eco verde en esquina inferior derecha
  - Radial gradient 2: centro en `(10%, 15%)`, color `--navy-800` al 30% de opacidad, radio 700px → aporta profundidad en esquina superior izquierda
  - Radial gradient 3 (opcional, muy sutil): centro en `(50%, 100%)`, color `--action-500` al 4% de opacidad, radio 500px → warmth muy tenue en la parte baja del hero (opcional, solo si aporta)
- **Textura de refuerzo** (una sola, no combinar):
  - **Opción A (recomendada)**: dot pattern SVG con dots de 1.5px, spacing 32px, color `rgba(255,255,255,0.04)`
  - **Opción B**: grid pattern SVG con líneas de 1px cada 80px, color `rgba(255,255,255,0.03)`
- **Sin overlay adicional**: al no haber video ni foto, no se necesitan capas de contraste

#### Layout Desktop (asimétrico, grid 12 columnas)

- **Padding**: `160px` top / `120px` bottom / `120px` horizontal
- **Columnas 1–7**: bloque de contenido textual (izquierda)
- **Columnas 8–12**: composición gráfica de productos (derecha)
- **Gap horizontal**: `48px` entre columnas de contenido y gráfico

#### Bloque de Texto (columnas 1–7)

**Badge component** (arriba del headline, alineado a izquierda):
- Píldora oscura `bg-slate-900/60` con `backdrop-blur-md` y borde `1px solid rgba(255,255,255,0.08)`
- Contenido interno con 2 partes:
  - Tag negra (`bg-slate-950 text-white`, radius `--radius-full`, padding `4px 10px`): `[Icono chispa] Nuevo`
  - Texto: `100% Biodegradable · NOM-018-STPS`
- Font: Inter Medium 13px, color `rgba(255,255,255,0.9)`
- Padding externo `6px 6px 6px 6px`, radius `--radius-full`, sombra `--shadow-sm`

**Headline principal** (34px de gap respecto al badge):
- Texto en 3 líneas explícitas:
  ```
  Insumos industriales.
  Estándar petrolero.
  Impacto ambiental cero.
  ```
- Font: Fustat Black (900), 88px desktop / 56px tablet / 44px mobile
- Line-height: `0.95`
- Tracking: `-4%` (approx `-3.5px` a 88px)
- Color: `#FFFFFF`
- Alineación: izquierda
- **Detalle de acento eco**: la palabra `cero.` de la tercera línea en color `--eco-500` (`#84CC16`) — esto crea un remate visual poderoso y refuerza la promesa de sustentabilidad en el último impacto tipográfico. Sin subrayados ni artificios adicionales.

**Subtítulo** (24px de gap respecto al headline):
- Texto: `Distribuidor B2B de productos de limpieza, kits de derrame y logística para la industria pesada del Golfo de México. Precios fijos, stock 24h, facturación CFDI 4.0.`
- Font: Inter Regular, 20px desktop / 17px mobile
- Line-height: `1.55`
- Tracking: `-0.3px`
- Color: `rgba(255,255,255,0.72)`
- Max-width: `540px` (deliberadamente estrecho para forzar quiebre de línea legible)

**Doble CTA** (40px de gap respecto al subtítulo, layout horizontal con gap 12px, colapsa a stack en mobile):
- **Primario**: `Solicitar Cotización`
  - `bg-[--action-500]` texto blanco
  - Padding `16px 28px`, altura `56px`, radius `--radius-md`, Inter SemiBold 16px
  - Ícono flecha derecha (16px) con animación `translateX(3px)` en hover
  - Hover: `bg-[--action-600]`, lift `translateY(-2px)`, sombra `--shadow-lg`
  - Focus: ring 2px `--action-500` con offset 2px sobre el fondo navy
- **Secundario**: `Chatear por WhatsApp`
  - `bg-white/8 backdrop-blur border border-white/20 text-white`
  - Mismas dimensiones, Inter SemiBold 16px
  - Ícono WhatsApp (16px) a la izquierda del texto
  - Hover: `bg-white/12`, borde `white/30`

**Trust markers pequeños** (24px de gap bajo los CTAs):
- 3 chips con separador `·` entre ellos, texto muy pequeño
- Contenido:
  - `[Ícono check] Sin costo · Sin compromiso`
  - `·`
  - `[Ícono reloj] Respuesta < 4h hábiles`
- Font: Inter Medium 13px, color `rgba(255,255,255,0.55)`
- Sin fondo, solo texto e íconos inline

#### Composición Gráfica (columnas 8–12)

**Objetivo**: mostrar recognición inmediata de producto sin fotografía, en un lenguaje visual que se sienta editorial y controlado. Ilustración vectorial flat con toque 2.5D (isometría muy ligera, no full iso).

**Elementos a componer** (todos como SVG vectorial editable, paleta reducida `--navy-950`, `--navy-800`, `--white`, `--eco-500`, con `--action-500` solo en pequeños acentos de hazard):

1. **IBC Tote de 1000L** (elemento hero, más grande, centro-derecha):
   - Jaula metálica en navy con detalles blancos
   - Líquido interno insinuado en azul muy tenue
   - Tag colgante flotante: `1,000 L` (Inter Bold 12px, chip blanco)
   
2. **Tambor 200L** (parte superior, escala menor):
   - Silueta clásica de tambor navy con banda superior blanca
   - Etiqueta hazard pequeña en `--action-500` (única aparición del naranja en la composición)
   
3. **Garrafa Swipe** (parte inferior izquierda del grupo):
   - Botella con silueta característica
   - Detalles en amarillo mostaza tenue + navy
   
4. **Kit de derrame compacto** (fondo, escala menor):
   - Contenedor amarillo con tapa negra
   - Absorbentes stylizados

**Composición espacial**:
- No alinear todo en una fila — usar profundidad con Z-index visual (algunos productos más adelante, otros más atrás)
- Rotación 0° (mantener rectitud para lectura B2B seria)
- Base flotante: sombras muy sutiles (`--shadow-sm` con blur alto y opacity baja) para desprender los objetos del fondo
- Sin outlines gruesos: usar shapes limpios con fills sólidos

**Trust tags flotantes** (elemento clave — 4 tags conectados a productos específicos):
- Cada tag es una píldora con glassmorphism:
  - `bg-white/8 backdrop-blur-md border border-white/15`
  - Radius `--radius-full`, padding `6px 12px`
  - Ícono + texto en Inter Medium 12px, color blanco
- Conexión al producto: línea ultra fina (1px, `rgba(255,255,255,0.2)`) que se extiende del borde del tag hasta un punto del producto correspondiente, terminando en un pequeño dot (3px) del color del acento
- Los 4 tags a incluir:
  1. `[Ícono hoja]` **100% Biodegradable** → conectado a la garrafa Swipe (dot verde eco)
  2. `[Ícono escudo]` **NOM-018-STPS** → conectado al kit de derrame (dot naranja)
  3. `[Ícono reloj]` **Stock 24h** → conectado al IBC (dot blanco)
  4. `[Ícono factura]` **CFDI 4.0** → conectado al tambor (dot blanco)
- Posiciones alrededor de la composición sin superponer productos

**Efecto de "instrucción técnica"**: la composición debe leerse como un exploded view o technical illustration de catálogo industrial premium (referencia visual: Muji product catalogs, Dieter Rams technical drawings, Studio Neat product shots). NO como render 3D fotorrealista.

#### Layout Mobile

- Stack vertical centrado
- Padding: `120px 24px 80px`
- Orden: Badge → Headline (44px, tres líneas) → Subtítulo → CTAs (stack full-width, primario arriba) → Trust markers → Composición gráfica simplificada (solo 2 productos: IBC + kit de derrame) con 2 tags flotantes
- La composición ocupa 100% del ancho y va debajo del bloque de texto
- Trust markers en una sola línea con `flex-wrap`

#### Configurador de Cotización Rápida — MOVIDO fuera del hero

**Cambio arquitectónico**: dado que el hero ya no tiene video ni un elemento "invitando a preguntar", el configurador se traslada a una sección independiente inmediatamente después del hero (antes del Trust Bar). Esto le da respiración, más peso conversional, y evita saturar el hero.

- **Fondo de la sección**: `--slate-50` (contraste amable después del navy del hero)
- **Padding**: `80px 0`
- **Contenedor**: max-width `1080px`, centrado
- **Card**:
  - `bg-white`, radius `--radius-2xl`, sombra `--shadow-xl`, borde `1px solid --slate-200`
  - Padding interno `48px` desktop / `24px` mobile
  - **Row superior (barra de contexto)**:
    - Layout: 2 columnas espaciadas
    - Izquierda: `[Ícono escudo verde] Distribuidor autorizado · RFC RMA240222RH7`
    - Derecha: `[Ícono reloj] Respuesta en menos de 4h hábiles`
    - Font: Schibsted Grotesk Medium 12px, `--slate-500`, uppercase, tracking +2%
    - Separador inferior 1px `--slate-200`, gap `24px`
  - **Título de la sección** (dentro de la card, después del separador):
    - Eyebrow: `COTIZACIÓN EN 60 SEGUNDOS` (`--action-500`, uppercase, 11px, tracking +3%)
    - H2: `Cuéntanos qué necesitas y te enviamos precio en horas.` (Fustat Bold 32px, `--navy-950`)
    - Sin subtítulo adicional para mantener directo
  - **Área de formulario**:
    - Layout grid 2 columnas desktop, 1 columna mobile, gap 20px
    - Campos:
      - **Selector**: `¿Qué necesitas cotizar?` → dropdown con opciones (Limpieza Industrial, Kit de Derrame & Seguridad, Tarimas & Totes, Insumos Institucionales, Mezcla / No estoy seguro)
      - **Input**: `Cantidad estimada / Frecuencia` (texto libre corto)
      - **Input**: `Correo corporativo` (con validación email inline)
      - **Input**: `Empresa` (texto)
    - Todos los campos: altura 52px, borde `1px solid --slate-300`, focus ring `--action-500`, radius `--radius-md`
  - **Botón CTA principal** (full-width bajo el grid, gap 24px):
    - `bg-[--action-500]` texto blanco, altura 56px, radius `--radius-md`, Inter SemiBold 16px
    - Texto: `Solicitar Cotización →`
    - Estado loading con spinner blanco cuando se envía
  - **Row inferior (acciones auxiliares)**:
    - 3 chip-buttons horizontales, `bg-slate-100 hover:bg-slate-200 radius-md padding 8px 14px`:
      - `[Ícono documento] Descargar Catálogo PDF`
      - `[Ícono MSDS] Ver Fichas MSDS`
      - `[Ícono WhatsApp] Contactar Ventas por WhatsApp`
    - Checkbox de consentimiento LFPDPPP (ver sección 10) debajo, con enlace al Aviso de Privacidad
  - **Micro-copy de cierre** (12px, `--slate-500`, alineado al centro):
    - `Tus datos están protegidos. Nunca los compartimos con terceros.`

---

### 6.3 Trust Bar

- **Fondo**: `slate-50`
- **Padding**: `48px 0`
- **Contenido**: Texto de intro pequeño arriba (`slate-500`, uppercase 12px, tracking +3%): "DISTRIBUIDOR AUTORIZADO DE"
- **Grid**: 8 logos en escala de grises (`grayscale opacity-60`), alineados horizontalmente con hover que restaura color
- **Marcas**: Swipe, 3M, Kimberly-Clark, Greenco, Truper, Kemix Bio, Prolimp, Elite
- **Mobile**: Slider horizontal con auto-scroll suave (respetando `prefers-reduced-motion`)

---

### 6.4 Grid de Soluciones (4 tarjetas)

- **Sección con fondo blanco**, padding vertical `120px`
- **Header**: 
  - Eyebrow: "SOLUCIONES INTEGRALES" (Schibsted Grotesk Medium 12px, `--eco-600`, tracking +3%)
  - H2: "Todo lo que tu operación necesita, un solo proveedor"
  - Subtítulo: párrafo corto centrado
- **Grid**: 2×2 en desktop, 1 col mobile, gap `24px`

**Card structure** (repetir 4 veces):
- Fondo: blanco
- Border: `1px solid slate-200`, hover `slate-300`
- Radius: `--radius-xl`
- Padding: `32px`
- Sombra default: `--shadow-sm`, hover: `--shadow-lg` + lift `translateY(-4px)` con transición `250ms cubic-bezier(0.4,0,0.2,1)`
- Contenido:
  - Ícono grande (48px, outline 2px, color `--navy-900`)
  - Tag categoría (chip pequeño con color acento según tipo)
  - H3 título
  - Descripción 2-3 líneas (`slate-500`)
  - Lista de 3-4 sub-productos con checkmark eco
  - Link "Ver soluciones →" con hover underline animado

**Contenido de las 4 cards**:

1. **Limpieza Industrial**
   - Tag: `[Verde eco]` "Biodegradable"
   - "Desengrasantes, multiusos y detergentes concentrados formulados para instalaciones industriales pesadas."
   - Sub: Swipe Magic · Greenco Green 1500 · Multiusos concentrado · Detergentes institucionales

2. **Seguridad & Kits de Derrame**
   - Tag: `[Naranja]` "Respuesta rápida"
   - "Kits completos para contención y limpieza de derrames de hidrocarburos y químicos. Cumplen NOM-018-STPS."
   - Sub: Kits universales · Absorbentes · EPP especializado · Contenedores HAZMAT

3. **Logística Industrial**
   - Tag: `[Azul]` "Cadena de suministro"
   - "Tarimas de madera, plástico y anti-derrame. Totes, tanques cerrados y contenedores para almacenamiento y transporte."
   - Sub: Tarimas maciza/multicapa · IBC 1000L · Tambos 200L · Supersacos

4. **Insumos Institucionales**
   - Tag: `[Verde eco]` "Alto rendimiento"
   - "Papel higiénico, toallas, jabones, dispensadores y consumibles para instalaciones con alto flujo de personal."
   - Sub: Kimberly-Clark · Elite Empresas · Dispensadores · Aromatizantes

---

### 6.5 Sección "Por qué RIOAZA" — Bento Grid

- **Fondo**: `--navy-950` con textura sutil (dot pattern al 3% opacity)
- **Padding**: `120px 0`
- **Header** (texto blanco):
  - Eyebrow: "POR QUÉ RIOAZA"
  - H2: "Seis razones por las que la industria del Golfo nos elige"
- **Bento layout** (grid 4×2 con celdas de tamaño variable, gap 16px):

| Celda | Tamaño | Contenido |
|---|---|---|
| 1 | 2×1 | **"100% Biodegradables"** — badge eco + descripción + ilustración pequeña de gota + hoja |
| 2 | 1×1 | **"Fichas MSDS de todo el catálogo"** — ícono documento + CTA descargar |
| 3 | 1×1 | **"Stock 24h"** — ícono reloj + métrica "48h entrega promedio" |
| 4 | 1×2 | **"Cobertura Golfo de México"** — Mapa estilizado del sureste con puntos: Cd. del Carmen, Coatzacoalcos, Villahermosa, Ciudad Madero |
| 5 | 1×1 | **"Facturación CFDI 4.0"** — ícono factura + "Emisión inmediata" |
| 6 | 1×1 | **"Precios fijos MXN"** — ícono candado + "Blindados vs. tipo de cambio" |
| 7 | 2×1 | **"Crédito a empresas"** — ícono handshake + "Líneas de crédito a 15/30/45 días previa evaluación" |

Cada celda:
- Fondo: `slate-900` con borde `1px solid slate-800`
- Radius: `--radius-xl`
- Padding: `32px`
- Hover: borde `slate-700`, ligero glow `--eco-500` al 10%

---

### 6.6 Sección "Sectores que Atendemos"

- **Fondo**: blanco
- **Layout**: Tabs con 4 pestañas (Petrolero · Marítimo · Portuario · Industrial)
- Cada tab muestra:
  - Imagen contextual del sector (foto real del sureste)
  - Lista de retos operativos que RIOAZA resuelve
  - Casos de uso: 2-3 productos recomendados por sector
  - Testimonio corto anónimo o con logo del cliente si se autoriza

---

### 6.7 Catálogo Destacado (Preview)

- **Header**: H2 "Productos más solicitados"
- **Grid**: 4 productos en desktop, 2 en tablet, 1 en mobile
- **Card producto**:
  - Imagen del producto sobre fondo `slate-50` con radius superior `--radius-xl`
  - Chip categoría (esquina superior izquierda)
  - Chip "Biodegradable" cuando aplique (`--eco-500`)
  - Nombre producto (Inter SemiBold 16px)
  - Marca (Inter Regular 14px, `slate-500`)
  - 2 botones: "Solicitar cotización" (naranja outline) + "Ficha MSDS" (ghost)
- **CTA sección**: "Ver catálogo completo →" alineado al centro

---

### 6.8 FAQ Técnico

- **Layout**: Acordeón de 2 columnas, 4 preguntas por columna
- **Preguntas sugeridas**:
  - ¿Emiten CFDI 4.0? ¿Con qué complementos?
  - ¿Cuál es el tiempo mínimo de entrega en zona de plataformas?
  - ¿Cuentan con hojas MSDS en español para cada producto?
  - ¿Manejan condiciones de crédito para nuevos clientes?
  - ¿Los productos biodegradables cumplen normativa PROFEPA?
  - ¿Pueden emitir facturas globales para contratos anuales?
  - ¿Ofrecen capacitación en uso de kits de derrame?
  - ¿Están dados de alta en CompraNet / padrones de proveedores?

---

### 6.9 Formulario de Cotización B2B (sección de conversión final)

- **Layout**: 2 columnas — izquierda formulario, derecha datos de contacto directo
- **Fondo**: `--navy-950` con overlay de patrón industrial sutil
- **Padding**: `96px 120px`

**Columna izquierda — Formulario**:

Card blanca con `--shadow-xl` y `radius-2xl`, padding `48px`.

- H2 (dentro de la card): "Solicita tu cotización"
- Subtítulo: "Respuesta garantizada en menos de 4 horas hábiles."
- Campos (todos con label persistente arriba, no floating):
  - **Nombre completo*** (text)
  - **Empresa*** (text)
  - **Correo corporativo*** (email — validación server-side + client-side)
  - **Teléfono / WhatsApp*** (tel — formato MX auto)
  - **Sector*** (select: Petrolero, Marítimo, Portuario, Industrial, Otro)
  - **¿Qué necesitas cotizar?*** (multi-select con las 4 categorías + textarea "Otro")
  - **Cantidad estimada / Frecuencia** (textarea)
  - **Zona de entrega*** (select con estados del sureste + "Otro")
- **Checkbox de consentimiento LFPDPPP** (obligatorio, unchecked por default):
  - "He leído y acepto el [Aviso de Privacidad](/privacidad). Autorizo el tratamiento de mis datos para fines de contacto comercial."
- **Honeypot field** oculto (nombre `website_url`, aria-hidden)
- **Cloudflare Turnstile** widget invisible
- **Botón submit**: "Enviar solicitud" (naranja, full-width, 56px altura, estado loading con spinner)
- Estados: default / focus (ring `--action-500` de 2px) / error (borde `--error` + mensaje debajo) / success (toast + redirect a `/gracias`)

**Columna derecha — Contacto directo**:

- Bloque con datos de la empresa:
  - "Ciudad del Carmen, Campeche"
  - Dirección fiscal completa
  - RFC visible
  - 3 contactos con nombre, cargo, teléfono, correo (los del CV)
  - Botón grande "WhatsApp Business" con verde `--success`

---

### 6.10 Footer

- **Fondo**: `--navy-950`
- **Layout**: 4 columnas + fila legal inferior
- Columnas:
  1. Logo + eslogan + redes sociales (LinkedIn, Facebook, Instagram)
  2. Soluciones (enlaces a categorías)
  3. Empresa (Nosotros, Sectores, Recursos, Blog)
  4. Legal (Aviso de Privacidad, Términos, RFC, Acta Constitutiva)
- **Fila inferior**: 
  - Copyright + año dinámico
  - Botón "↑ Volver arriba"
  - Micro-texto: "Sitio construido con estándares WCAG 2.2 AA. LFPDPPP compliant."

---

## 7. INTERACCIONES Y MICRO-INTERACCIONES

**Filosofía v1**: Solo micro-interacciones de estado. Sin animaciones de scroll, sin parallax, sin video, sin motion decorativo. Cada transición debe existir por función (feedback de estado, jerarquía de acción). El objetivo es que la landing se sienta rápida, sobria y controlada — no cinematográfica.

**Reglas globales**:
- Duración estándar: `200ms` para hover y cambios de color, `300ms` para elevación
- Easing por defecto: `cubic-bezier(0.4, 0, 0.2, 1)` (ease-out-quart)
- Respetar `prefers-reduced-motion: reduce` — sustituir transiciones por cambios instantáneos, mantener funcionalidad

**Estados obligatorios en todos los componentes interactivos**:
- Default
- Hover (elevación sutil + cambio de color)
- Focus (ring 2px `--action-500` con offset 2px — accesibilidad de teclado, obligatorio)
- Active (compresión sutil `scale(0.98)`)
- Disabled (`opacity 0.5`, cursor `not-allowed`)
- Loading (spinner o skeleton, no bloquear UI completa)
- Error (borde `--error`, mensaje debajo con `aria-live="polite"`)

**Micro-interacciones específicas permitidas en v1**:
- Nav bar: transición `background` + `backdrop-blur` cuando `scrollY > 80px` (300ms). Es la única "reacción al scroll" permitida.
- Cards de soluciones: lift `translateY(-4px)` + sombra escalada en hover (200ms)
- Botones CTA: cambio de color de fondo + micro-lift `translateY(-2px)` en hover
- Wordmark del navbar: transición sutil del dot verde de `--eco-500` a `--eco-600` en hover
- Trust tags del hero: sin animación de entrada, aparecen en su posición final
- Formulario: validación en tiempo real con feedback inmediato bajo el campo (sin animaciones de shake ni bounce)
- Acordeón de FAQ: expand/collapse con transición de altura (300ms)

**Explícitamente prohibido en v1**:
- Animaciones de entrada activadas por `IntersectionObserver`
- Parallax de cualquier tipo
- Números que "cuentan hacia arriba" en métricas
- Cursors personalizados
- Confetti, sparkles, o cualquier animación decorativa
- Auto-play de carruseles con timing agresivo

---

## 8. COPY COMPLETO (Español B2B Mexicano)

### Hero
- **Badge**: `Nuevo · 100% Biodegradable · NOM-018-STPS`
- **H1**: `Insumos industriales.\nEstándar petrolero.\nImpacto ambiental cero.`
- **Subtítulo**: `Distribuidor B2B de productos de limpieza, kits de derrame y logística para la industria pesada del Golfo de México. Precios fijos, stock 24h, facturación CFDI 4.0.`
- **CTA 1**: `Solicitar Cotización →`
- **CTA 2**: `Chatear por WhatsApp`

### Trust Bar
- `Distribuidor autorizado de las marcas que la industria exige`

### Grid Soluciones
- **Eyebrow**: `SOLUCIONES INTEGRALES`
- **H2**: `Todo lo que tu operación necesita, un solo proveedor`
- **Subtítulo**: `Consolida tu compra de limpieza, seguridad y logística con un proveedor certificado, con inventario disponible y respuesta en cuestión de horas.`

### Bento
- **Eyebrow**: `POR QUÉ RIOAZA`
- **H2**: `Seis razones por las que la industria del Golfo nos elige`

### Formulario
- **H2**: `Solicita tu cotización`
- **Subtítulo**: `Respuesta garantizada en menos de 4 horas hábiles.`
- **Confirmación post-submit**: `Recibimos tu solicitud. Un ejecutivo de RIOAZA te contactará en máximo 4 horas hábiles. Si tu solicitud es urgente, escríbenos por WhatsApp.`

### Errores
- Campo requerido: `Este campo es obligatorio`
- Email inválido: `Ingresa un correo válido`
- Consentimiento: `Debes aceptar el aviso de privacidad para continuar`
- Error servidor: `Ocurrió un error. Intenta de nuevo o contáctanos por WhatsApp.`

---

## 9. ACCESIBILIDAD (WCAG 2.2 AA — obligatorio)

- Contraste mínimo 4.5:1 para texto normal, 3:1 para texto grande y elementos gráficos
- Focus rings visibles siempre (nunca `outline: none` sin reemplazo)
- Navegación 100% funcional por teclado (Tab, Shift+Tab, Enter, Escape para modales)
- `aria-label` en todos los botones con solo ícono
- `aria-live` en mensajes de validación de formulario
- `<label>` asociado con `for` a cada input
- Alt text descriptivo en todas las imágenes; `alt=""` en decorativas
- Skip link "Saltar al contenido principal" al inicio del `<body>`
- Semántica HTML5 correcta (`<header>`, `<nav>`, `<main>`, `<section>`, `<footer>`)
- Composición gráfica del hero: todos los elementos SVG con `aria-hidden="true"` (decorativos). Los trust tags flotantes con texto son parte del contenido informativo y sí se leen por screen readers.
- Formularios: mensajes de error asociados con `aria-describedby`

---

## 10. SEGURIDAD Y CUMPLIMIENTO LEGAL

### Protección del formulario
- **Cloudflare Turnstile** (invisible) como anti-bot primario
- **Honeypot field** (`website_url`) como capa secundaria
- **Rate limiting** en el endpoint API: 5 requests por IP cada 10 minutos
- **Validación**:
  - Client-side con Zod (feedback rápido)
  - Server-side obligatoria en el route handler (Zod schema idéntico)
  - Sanitización con `DOMPurify` o equivalente
- **CSRF token** en endpoints mutantes

### Headers HTTP obligatorios
```
Content-Security-Policy: default-src 'self'; script-src 'self' 'nonce-{}' https://challenges.cloudflare.com; style-src 'self' 'unsafe-inline'; img-src 'self' data: https:; connect-src 'self' https://api.rioaza.mx; frame-ancestors 'none';
Strict-Transport-Security: max-age=63072000; includeSubDomains; preload
X-Content-Type-Options: nosniff
X-Frame-Options: DENY
Referrer-Policy: strict-origin-when-cross-origin
Permissions-Policy: camera=(), microphone=(), geolocation=()
```

### LFPDPPP (Ley Federal de Protección de Datos Personales en Posesión de los Particulares)
- Aviso de Privacidad completo accesible desde footer y desde el formulario
- Consentimiento explícito antes de submit (checkbox unchecked por default)
- Solo capturar datos necesarios para el fin declarado (minimización)
- Definir política de retención (sugerido: 24 meses con opción de solicitar borrado)
- Contacto de DPO o responsable de datos visible
- Banner de cookies con consentimiento previo si se usa analítica

### Analítica
- Preferir soluciones privacy-first (Plausible, Fathom, Umami) sobre Google Analytics
- Si se usa GA4: consentimiento previo obligatorio, IP anonymization, sin remarketing sin opt-in

---

## 11. RESPONSIVE — Reglas Mobile-First

- **Diseñar primero para 375px** (iPhone estándar), luego escalar hacia arriba
- Hero en mobile: H1 baja a 44px, composición gráfica se simplifica a 2 productos, configurador de cotización se muestra completo en su sección independiente inmediatamente después
- Nav mobile: hamburger drawer con overlay + backdrop-blur
- Grid soluciones: 1 columna
- Bento: colapsa a stack vertical con proporciones ajustadas
- Formulario: campos full-width, botón sticky en bottom del viewport durante scroll dentro del form
- Tap targets mínimos: 44×44px (guideline Apple/Google)
- Font sizes: nunca menores a 14px en body

---

## 12. PERFORMANCE (targets)

- **Lighthouse Performance**: ≥ 90 mobile, ≥ 95 desktop
- **LCP**: < 2.0s
- **CLS**: < 0.05
- **INP**: < 200ms
- **Composición gráfica del hero**: SVG inline optimizado con `svgo`, peso combinado del hero (SVG + fondos + gradients) máximo 40KB. Sin PNG raster en la composición.
- **Imágenes**: WebP con AVIF fallback, dimensiones explícitas siempre para evitar CLS, `loading="lazy"` en todo lo que esté fuera del above-the-fold
- **Fuentes**: `font-display: swap`, precargar solo Fustat 700 y Inter 400/500/600
- **JavaScript**: code-splitting por ruta, dynamic imports para modales, no bloquear render
- **CSS**: purge de Tailwind agresivo, critical CSS inline en `<head>`

---

## 13. ENTREGABLES ESPERADOS

Al ejecutar este prompt, quiero recibir:

1. **Diseño visual completo** de la landing en desktop (1440px) y mobile (375px)
2. **Design tokens** exportables (JSON o Tailwind config)
3. **Componentes React** (Next.js 15 App Router + shadcn/ui) organizados en la siguiente estructura:

```
components/
├── ui/            # Primitivos shadcn
├── sections/      # HeroSection, HeroGraphicComposition, 
│                  # QuoteConfiguratorSection, TrustBar, SolutionsGrid, 
│                  # BentoWhy, SectorsTabs, CatalogPreview, 
│                  # FaqTechnical, QuoteForm, Footer
├── forms/         # QuoteForm con Zod + server actions
└── layout/        # Navbar, MobileDrawer, Container
```

4. **Route handler** del formulario con Turnstile + rate limit + Zod
5. **Middleware** con headers de seguridad
6. **README** con instrucciones de setup, variables de entorno necesarias, y checklist de contenido pendiente

---

## 14. QUÉ NO HACER (Anti-patrones)

- ❌ No usar el naranja `--action-500` fuera de CTAs y alertas
- ❌ No mezclar copy B2B con lenguaje de e-commerce ("agregar al carrito", "compra ya")
- ❌ No usar stock photography en el hero — la composición debe ser 100% SVG vectorial ilustrado
- ❌ No usar fotos genéricas de gente sonriendo con laptops en NINGUNA sección
- ❌ No renderizados 3D fotorrealistas en la composición del hero — mantener estética flat/2.5D editorial
- ❌ No emojis en copy formal
- ❌ No parallax, scroll hijacking, ni animaciones activadas por scroll en v1
- ❌ No usar la mascota del logo en el navbar (solo wordmark simplificado)
- ❌ No usar naranja `--action-500` fuera de CTAs, alertas y stickers hazard en la ilustración del hero
- ❌ No modales que interrumpen el scroll inicial (exit-intent está OK después de 30s en página)
- ❌ No formularios de más de 8 campos en la etapa de captura inicial
- ❌ No usar `#84CC16` como fondo de botón con texto blanco (falla contraste AA — usar `--eco-600`)
- ❌ No omitir el checkbox LFPDPPP (obligatorio legal en México)
- ❌ No usar el logo actual en producción sin re-trazarlo como SVG vectorial editable

---

**Fin del prompt. Ejecuta con criterio de diseñador senior. Cuando tengas dudas de contenido específico, asume el default más profesional posible y márcalo para revisión posterior.**
