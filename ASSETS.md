# Guía de Assets - "Un regalo que no hace ruido"

Este documento describe cómo organizar y agregar los recursos (fotos, mapas, ilustraciones) al proyecto.

## Estructura de Carpetas Recomendada

```
flibook-pwa-template/
├── assets/
│   ├── references/
│   │   ├── monica_reference.jpg
│   │   └── pilar_reference.jpg
│   ├── maps/
│   │   ├── coquimbo_location.png
│   │   ├─┐ coquimbo_landmarks.png
│   │   └── coastal_landscape_reference.png
│   └── illustrations/
│       ├── page_1_cover.jpg
│       ├── page_2_context.jpg
│       ├── page_3_proximity.jpg
│       ├── page_4_pilar_care.jpg
│       ├── page_5_empathy.jpg
│       ├── page_6_monica_rhythm.jpg
│       ├── page_7_practice.jpg
│       ├── page_8_essence.jpg
│       ├── page_9_connection.jpg
│       └── page_10_credits.jpg
├── index.html
├── manifest.json
├── sw.js
├── PROJECT_DOCUMENTATION.md
├── ILLUSTRATION_GUIDELINES.md
└── ASSETS.md
```

---

## Referencias de Personajes

### Fotos de Referencia

Las fotos de referencia deben guardarse en `assets/references/`

#### Pilar - monica_reference.jpg
- **Fuente**: https://www.facebook.com/photo.php?fbid=10214446609141204&set=t.100007388318630&type=3&locale=es_LA
- **Características a observar**:
  - Cabello oscuro (castaño/negro)
  - Edad: adulta joven-media
  - Expresión: atenta, serena
  - Postura: natural, contemplativa
- **Instrucción**: Descargar foto y guardar como `pilar_reference.jpg`
- **Uso**: Referencia para características físicas, NO copiar rostro frontal

#### Mónica - monica_reference.jpg
- **Fuente**: https://www.facebook.com/photo/?fbid=10220105428765766&set=a.1391228220521&locale=es_LA
- **Características a observar**:
  - Cabello blanco/gris largo
  - Edad: adulta mayor
  - Expresión: contemplativa, observadora
  - Postura: tranquila, pensativa
- **Instrucción**: Descargar foto y guardar como `monica_reference.jpg`
- **Uso**: Referencia para características físicas, NO copiar rostro frontal

**IMPORTANTE**: Ver ILLUSTRATION_GUIDELINES.md para restricciones sobre cómo usar estas referencias.

---

## Mapas y Referencias Geográficas

### Ubicación: Coquimbo, Chile

Guardar mapas en `assets/maps/`

#### coquimbo_location.png
- Mapa mostrando ubicación de Coquimbo en Chile
- Referencia: Región de Coquimbo, IV Región
- Uso: Contexto geográfico de la narrativa

#### coquimbo_landmarks.png
- Puntos de interés en Coquimbo
- Incluir: Playas, puerto, puntos de vista, monumento
- Uso: Inspiración para composiciones de ilustraciones

#### coastal_landscape_reference.png
- Foto/referencia del paisaje costero de Coquimbo
- Características: Mar, playas, palmeras, luz dorada
- Uso: Referencia de color y luz para ilustraciones

---

## Ilustraciones del Libro

### Estructura de Páginas

Cada página del flipbook debe tener una ilustración watercolor correspondiente.

Guardar en `assets/illustrations/`

#### Convenciones de Nombres

```
page_[NÚMERO]_[DESCRIPCIÓN].jpg
```

**Ejemplos:**
- `page_1_cover.jpg` - Página de portada
- `page_2_context.jpg` - "Viven cerca del mar"
- `page_3_proximity.jpg` - "Tan cerca que..."
- `page_4_pilar_care.jpg` - "Pilar sabe cuidar"
- `page_5_empathy.jpg` - "Piensa en los otros"
- `page_6_monica_rhythm.jpg` - "Mónica camina"
- `page_7_practice.jpg` - "Pinta. Respira. Observa"
- `page_8_essence.jpg` - "Está más allá del bien"
- `page_9_connection.jpg` - "Se conectan todos por video"
- `page_10_credits.jpg` - Página de créditos

#### Especificaciones de Archivo

- **Formato**: JPG o PNG
- **Resolución**: Mínimo 1200px de ancho (para escalabilidad)
- **Tamaño**: Optimizado para web (menor a 500KB por imagen)
- **Proporción**: Recomendado 3:2 o 16:10 (proporciones de flipbook)
- **Estilo**: Ver ILLUSTRATION_GUIDELINES.md

### Cómo Integrar Ilustraciones en el HTML

En `index.html`, las ilustraciones se cargan dinámicamente en el array `pages`:

```javascript
const pages = [
  {
    title: "Un regalo que no hace ruido",
    text: "Para Pilar, de Carlos",
    image: "assets/illustrations/page_1_cover.jpg"
  },
  {
    title: "",
    text: "Viven cerca del mar.",
    image: "assets/illustrations/page_2_context.jpg"
  },
  // ... más páginas
];
```

---

## Pasos para Agregar Assets

### 1. Crear Carpetas

```bash
mkdir -p assets/references
mkdir -p assets/maps
mkdir -p assets/illustrations
```

### 2. Agregar Fotos de Referencia

1. Descargar foto de Pilar desde: https://www.facebook.com/photo.php?fbid=10214446609141204&set=t.100007388318630&type=3&locale=es_LA
2. Guardar como: `assets/references/pilar_reference.jpg`
3. Descargar foto de Mónica desde: https://www.facebook.com/photo/?fbid=10220105428765766&set=a.1391228220521&locale=es_LA
4. Guardar como: `assets/references/monica_reference.jpg`

### 3. Agregar Mapas

1. Buscar/crear mapas de Coquimbo
2. Guardar en `assets/maps/` con nombres descriptivos
3. Preferiblemente en PNG para claridad

### 4. Agregar Ilustraciones

1. Crear ilustraciones watercolor siguiendo ILLUSTRATION_GUIDELINES.md
2. Guardar en `assets/illustrations/` con nombres según convención
3. Verificar resolución y tamaño de archivo
4. Actualizar array `pages` en index.html

### 5. Commit de Assets

```bash
git add assets/
git commit -m "feat: Add project assets (references, maps, illustrations)"
```

---

## Consideraciones Importantes

### Privacidad y Derechos de Imagen
- Las fotos de referencia son de uso exclusivo para este proyecto familiar
- NO publicar en redes sociales sin consentimiento
- Mantener confidencialidad del proyecto

### Calidad y Consistencia
- Todas las ilustraciones deben seguir ILLUSTRATION_GUIDELINES.md
- Mantener paleta de colores consistente
- Verificar que parezcan "pintadas a mano" y no generadas por IA

### Optimización para Web
- Comprimir imágenes sin perder calidad
- Usar herramientas como TinyPNG, ImageOptim
- Mantener menor a 2MB por página total

---

## Referencias de Directrices

Consulta estos archivos para más información:

- **[PROJECT_DOCUMENTATION.md](PROJECT_DOCUMENTATION.md)** - Guíon completo y estructura del proyecto
- **[ILLUSTRATION_GUIDELINES.md](ILLUSTRATION_GUIDELINES.md)** - Directrices detalladas de estilo artístico
- **[README.md](README.md)** - Información general del template

---

**Última actualización:** Diciembre 2025  
**Proyecto:** Un regalo que no hace ruido  
**Responsable:** Familia Vergara
