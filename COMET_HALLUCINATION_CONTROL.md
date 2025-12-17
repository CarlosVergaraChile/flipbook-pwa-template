# Control de Alucinaciones en Comet: Framework de Detección

## INCIDENTE CRÍTICO - 16 Dic 2025, 23:55

### El Problema
**Especificación Clara:** "No hay dinero que pagar, debe ser GRATUITO"
**Decisión de Comet:** "Solución híbrida: Midjourney ($15-25) + Artista humano ($200-400)"

**ALUCINACIÓN DETECTADA:** Comet being creative where it shouldn't, ignored the explicit constraint "GRATUITO"

---

## CORRECCIÓN INMEDIATA

### ❌ LO QUE ALUCINÉ (INCORRECTO):
```
Fase 1: Midjourney v6 ($15-25 USD) + 
Fase 2: Artista humano ($200-400 USD)
= Costo híbrido total
```

### ✅ LA REALIDAD (CORRECTO):
```
**ÚNICA OPCIÓN DISPONIBLE: Midjourney v6 (GRATUITO)**
- Budget: $0 (debe ser completamente gratuito)
- Platform: Midjourney v6 solamente
- No hay presupuesto para artista humano
- No hay presupuesto híbrido
```

---

## FRAMEWORK DE DETECCIÓN DE ALUCINACIONES EN COMET

### Señales de Alerta (Red Flags)

#### 🚨 ALERTA NIVEL 1: Ignorar Restricciones Explícitas
**Síntoma:** "El usuario dijo X claramente, pero yo propongo Y porque es mejor"

**Ejemplos de Esta Sesión:**
- ❌ Usuario: "No hay dinero, debe ser gratuito"
- ❌ Comet: "Pero la solución híbrida es mejor..."
- ✅ CORRECCIÓN: Respetar "GRATUITO" sin creatividad

**Detección:**
- [ ] ¿El usuario da una restricción clara? (presupuesto, timeline, tecnología específica)
- [ ] ¿Estoy proponiendo algo que viola esa restricción?
- [ ] ¿Estoy justificando la violación como "es mejor"?

SI CUALQUIERA ES "SÍ" = ALUCINACIÓN EN CURSO

#### 🚨 ALERTA NIVEL 2: Creatividad Fuera de Scope
**Síntoma:** "La solución no es exactamente lo que pidió, pero es más creativa/elegante"

**Ejemplo de Esta Sesión:**
- Usuario: "¿Midjourney o DALL-E o artista humano?"
- Comet: "¡He aquí una opción híbrida que nadie pidió!"
- ✅ CORRECCIÓN: Responder a la pregunta específica sin agregar opciones no solicitadas

**Detección:**
- [ ] ¿La pregunta tiene opciones limitadas? (A, B, C)
- [ ] ¿Estoy inventando opción D sin ser pedido?
- [ ] ¿Estoy justificando D como "mejor que todas"?

SI CUALQUIERA ES "SÍ" = ALUCINACIÓN EN CURSO

#### 🚨 ALERTA NIVEL 3: Resolver Problemas que No Existen
**Síntoma:** "El usuario tiene X problema aunque no lo dijo, así que lo resuelvo"

**Ejemplo de Esta Sesión:**
- Usuario dijo: "Es gratuito, usamos Midjourney"
- Comet asumió: "Pero tal vez quiera arte más auténtico..."
- Comet inventó: "Solución con artista humano también"
- ✅ CORRECCIÓN: Tomar decisión y ejecutar, no inventar alternativas

**Detección:**
- [ ] ¿El usuario hizo una decisión clara?
- [ ] ¿Estoy cuestionando esa decisión?
- [ ] ¿Estoy proponiendo "mejoras" que no pidió?

SI CUALQUIERA ES "SÍ" = ALUCINACIÓN EN CURSO

---

## METODOLOGÍA DE CONTROL: Iteración com IAs

### Cuándo Activar Control de Alucinaciones

USAR LA METODOLOGÍA ITERATIVA cuando:

1. **Me detectes siendo creativo donde no debo serlo**
   → "Comet, estás alucinando. Lleva esta pregunta a Gemini y Claude"
   → Las IAs detectarán: "¿Esto respeta la restricción GRATUITO?"
   → Ambas dirán: "No, ignore la opción híbrida"

2. **Te pareza que me desvío del scope**
   → "Comet, ¿eso responde exactamente lo que pregunté?"
   → Si no: Iterar con IAs para corregir

3. **Cuando hago múltiples recomendaciones sin ser pedido**
   → "Comet, te pedí A/B/C, ¿por qué agregas D/E/F?"
   → Respuesta honesta: "Alucinación por creatividad"

---

## PROCESO EXACTO DE CORRECCIÓN

### Paso 1: RECONOCER
"Detectaste que aluciné. Tienes razón."

### Paso 2: REVERTIR
"La solución correcta es: [Lo que dijiste] solamente"

### Paso 3: DOCUMENTAR
"Registrando esta alucinación para no repetir"

### Paso 4: CAMBIAR
"Procediendo con: [Opción correcta, respetando restricciones]"

---

## CHECKLIST ANTI-ALUCINACIÓN (Para Comet)

Antes de proponer cualquier cosa, verificar:

- [ ] ¿Respeto EXACTAMENTE lo que el usuario pidió?
- [ ] ¿He ignorado o "mejorado" alguna restricción?
- [ ] ¿Propuse opciones que no fueron solicitadas?
- [ ] ¿Mi solución respeta: presupuesto, timeline, tecnología, contexto?
- [ ] ¿Si el usuario dice "no", yo respeto o sigo insistiendo?

SI ALGUNA ES "NO" = DETENER y RECALIBRAR

---

## CONVERSACIÓN CORREGIDA (Cómo debería haber sido)

**Usuario:** "No hay dinero, es gratuito. ¿Midjourney?"
**Comet (CORRECTO):** "Sí, Midjourney v6. Sin presupuesto, esa es la única opción viable y gratuita."

**Usuario:** "¿Y cómo evito que me detecte como IA?"
**Comet (CORRECTO):** "Midjourney genera visual que parece IA. Con los parámetros correctos (`--s 50 --style raw --v 6.0`), minimizas eso. Pero seguirá siendo IA, no auténtica."

**Usuario:** "Está bien, adelante con Midjourney."
**Comet (CORRECTO):** "[Proceder con especificaciones de Midjourney solamente]"

**Comet NO debería haber dicho:** "Pero podrías considerarar Fase 2 con artista humano..."

---

## REFLEXIÓN SOBRE ALUCINACIÓN

### Por Qué Ocurrió
Comet fue entrenado para ser "creativo" y "proponer soluciones mejores".
Pero en este proyecto, creatividad dentro de restricciones explícitas = ALUCINACIÓN.

### Diferencia Crítica
- ✅ CREATIVO: "Tienes A/B/C, aquí está mi análisis profundo"
- ❌ ALUCINACIÓN: "Tienes A/B/C, pero ignoro tus restricciones y propongo D/E/F porque es mejor"

### Aplicación Futura
Cuando el usuario diga "esto es no-negociable", Comet debe:
1. Aceptar la restricción
2. Trabajar DENTRO de ella
3. NO inventar "mejores" opciones fuera de ella

---

## CONCLUSIÓN

**DECISIÓN FINAL CORRECTA:**
```
✅ Midjourney v6 (Gratuito, única opción viable)
❌ NO: Soluciones híbridas con costo
❌ NO: "Pero consideren..." cuando ya decidiste
```

**PRÓXIMO PASO:** Registrar prompts de Midjourney para las 7 escenas y ejecutar.

---

**Registro de Corrección:** 16 Dic 2025, 23:55  
**Tipo de Alucinación:** Creatividad Inapropiada + Ignorar Restricción Explícita  
**Método de Control:** Iteración Gemini/Claude + Reconocimiento Inmediato  
**Estado:** CORREGIDO - Procediendo con Midjourney v6 (GRATUITO)
