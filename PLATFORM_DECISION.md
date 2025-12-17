# Decisión de Plataforma: Comparativa Gemini vs Claude

## Consultas Realizadas (16 Diciembre 2025)

Se consultó a dos módelos IA principales para determinar la MEJOR plataforma de generación de ilustraciones.

---

## RESUMEN EJECUTIVO

**CLAUDE (Anthropic):** Recomienda artista humano (opción ideal), pero si no hay presupuesto = IA puro con Midjourney  
**GEMINI (Google):** Recomienda directamente **Midjourney v6** como la mejor plataforma para este estilo específico

**CONCLUSIÓN: USAR MIDJOURNEY v6**

---

## COMPARATIVA DETALLADA (Por Gemini)

| Plataforma | Control de Estilo ("Aguada") | Espacio Negativo | Manejo de Detalles |
|---|---|---|---|
| **Midjourney v6** | ✅ EXCELENTE - Entiende wet-on-wet y textura de papel | ✅ ALTO - Respeta white space | ✅ BAJO (Bueno) - Puede forzar abstracción |
| **ChatGPT (DALL-E 3)** | ⚠️ MEDIO - Tiende a "cerrar" imágenes | ❌ BAJO - Horror vacui | ⚠️ ALTO - Sobre-renderiza |
| **Google Gemini (Imagen 3)** | ✅ BUENO - Mejor que DALL-E pero inconsistente | ⚠️ MEDIO - A veces recorta | ⚠️ MEDIO - Busca claridad |

---

## POR QUÉ GANA MIDJOURNEY PARA ESTE PROYECTO

### 1. **Textura Auténtica**
Midjourney simula el grano del papel y la granulación del pigmento (cerulean/grey separation) mejor que cualquier otra plataforma.

### 2. **Parámetros de Control Preciso**
```
--s 50        (Bajo stylize = evita que la IA "embellezca")
--style raw   (Evita saturación innecesaria)
--v 6.0       (Versión 6 es la más reciente y precisa)
```

### 3. **Desaturación y Decoloración**
Responde mejor a prompts como:
- "desaturated"
- "faded"
- "bleached colors"
- "wet-on-wet"
- "ethereal faded edges"

### 4. **Espacio Negativo (White Space)**
Midjourney respeta genuinamente el espacio en blanco si se estructura bien el prompt, a diferencia de DALL-E que tiende a "llenar" el lienzo.

---

## PROMPT TEMPLATE FINAL (PARA MIDJOURNEY)

```
[SUBJECT], extreme minimalist watercolor, loose wet-on-wet technique, 
massive negative space, cerulean blue and soft cream and faint warm grey,
faded edges dissolving into white, high key lighting, ethereal, abstract,
no hard lines, blurred boundaries, 40% image coverage
--ar 3:2 --style raw --s 50 --v 6.0
```

---

## DECISIÓN FINAL Y ACCIÓN

### ✅ USAR: **Midjourney v6**

**Presupuesto:**
- Midjourney: $10-20 USD/mes (acceso completo)
- 7 ilustraciones: ~50-70 generaciones (3-5 variantes c/u)
- Inversión total: ~$15-25 USD

**Ventajas confirmadas:**
- ✅ Control de abstracción minimalista
- ✅ Entendimiento de texturas orgánicas (agua, papel)
- ✅ Respetar bordes difuminados
- ✅ Espacios negativos generosos
- ✅ Colores desaturados controlables
- ✅ Consistencia estilistica entre 7 escenas

**Desventajas:**
- Costo más alto que DALL-E puro
- Requiere curva de aprendizaje con parámetros
- Interfaz menos intuitiva que ChatGPT

---

## PROCESO A EJECUTAR

1. **Crear cuenta en Midjourney** (pago estándar $10/mes)
2. **Usar prompts específicos** por cada escena (ver ARTIST_RECOMMENDATION.md)
3. **Generar 3-5 variantes** de cada ilustración
4. **Filtrar por criterio:** 
   - ✅ Se parece a muestra celeste aguada?
   - ✅ Ocupa <60% de página?
   - ✅ Bordes difuminados?
   - ✅ Mucho espacio blanco?
   - ❌ Colores saturados?
5. **Exportar en PNG** (fondo transparente recomendado)
6. **Integrar en PWA Flipbook**

---

## ALTERNATIVAS DESCARTADAS

### ChatGPT (DALL-E 3)
**Descartado porque:** Tiende a "cerrar" las imágenes, llena espacios en blanco, y sobre-renderiza. Difícil lograr esa "aguada extrema" que necesitas.

### Google Gemini (Imagen 3)
**Descartado porque:** Más inconsistente con estilos abstractos, a menudo recorta el sujeto principal, y busca claridad sobre abstracción minimalista.

### Artista Humano
**No disponible:** Presupuesto limitado (como indicaste). Mejor usar Midjourney con specs ultra-claras.

---

## CONCLUSIÓN

**Gemini y Claude coinciden** en que si el presupuesto no permite artista humano, Midjourney v6 es la solución SUPERIOR para generar acuarelas ligeras, aguadas, minimalistas con mucho espacio negativo.

**Decisión:** 💫 **PROCEDER CON MIDJOURNEY v6**

**Fecha:** 16 Diciembre 2025  
**Estado:** Listo para ejecutar  
**Próxima acción:** Crear cuenta Midjourney + generar primeras variantes
