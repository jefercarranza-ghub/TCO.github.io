# 🎯 TCO Pro - Guía Comercial de Uso

## 📋 Resumen Ejecutivo

**TCO Pro** es tu herramienta de **cierre consultivo**. No vende equipos, vende **valor demostrado con datos**. 

- ✅ Compara **3-8 equipos simultáneamente** (no solo 2)
- ✅ Importa tus propios datos de modelos
- ✅ Ajusta variables comerciales en tiempo real (volumen, energía, horas)
- ✅ Genera recomendaciones automáticas basadas en TCO
- ✅ Desglose transparente de costos por componente

---

## 🚀 Cómo Empezar (5 minutos)

### Paso 1: Abre la herramienta
`comparador-tco-pro.html` en tu navegador. No requiere internet ni instalación.

### Paso 2: Ajusta los parámetros base
En la sección **"Parámetros de Cálculo"**, modifica:

| Parámetro | Descripción | Ejemplo |
|-----------|-------------|---------|
| **Volumen mensual** | Páginas/mes que imprime el cliente | 50,000 (SME educativa) |
| **Horas/día** | Operación diaria del equipo | 8 (1 turno) o 16 (2 turnos) |
| **Días/mes** | Días laborales | 22 (Perú estándar) |
| **Tarifa energía** | $/kWh según zona | $0.12 (Lima), $0.18 (industrial) |

**✅ Estos 4 números definen toda la economía.**

### Paso 3: Selecciona equipos a comparar
Haz click en los botones de equipo. Puedes comparar hasta 8 simultáneamente.

Vienen 8 modelos por defecto:
- Sharp BP-70M65A, MX-M487F
- Ricoh MP C6502, MP C3503
- Kyocera TASKalfa 8580
- Xerox Versant 280
- RISO Valezus T2200
- Canon imageRUNNER LR

### Paso 4: Lee los 3 tabs
1. **Dashboard** → KPIs visuales + desglose de costos
2. **Comparativa** → Tabla TCO (12, 24, 36 meses)
3. **Detalles** → Specs técnicas y comerciales de cada equipo

---

## 💾 Importar Tus Propios Equipos

**Caso de uso:** Tienes modelos Sharp con precios actualizados o nuevos proveedores.

### Paso 1: Haz click en "⬆ Importar"

Se abrirá un textarea con placeholder JSON.

### Paso 2: Prepara tu JSON

Pega un array con este formato:

```json
[
  {
    "id": "sharp-nuevo-1",
    "name": "Sharp MX-M550N",
    "brand": "Sharp",
    "ppm": 55,
    "consumoKwh": 1.5,
    "rentaMensual": 750,
    "costClick": 0.012,
    "costPaper": 0.02,
    "voltageStable": true
  },
  {
    "id": "xerox-custom",
    "name": "Xerox AltaLink C8070",
    "brand": "Xerox",
    "ppm": 70,
    "consumoKwh": 2.2,
    "rentaMensual": 1150,
    "costClick": 0.0115,
    "costPaper": 0.021,
    "voltageStable": true
  }
]
```

**Explicación de campos:**

| Campo | Significado | Ejemplo |
|-------|-------------|---------|
| `id` | ID único (sin espacios) | `sharp-bp65` |
| `name` | Nombre comercial | `Sharp BP-70M65A` |
| `brand` | Marca para filtrar | `Sharp`, `Ricoh`, etc. |
| `ppm` | Páginas por minuto | `65` |
| `consumoKwh` | Consumo energético por hora | `1.8` |
| `rentaMensual` | Renta/leasing mensual | `850` (USD) |
| `costClick` | Costo por página impresa | `0.012` (USD/pág) |
| `costPaper` | Costo de papel/consumible | `0.02` (USD/pág) |
| `voltageStable` | ¿Requiere estabilizador? | `true` o `false` |

### Paso 3: Click en "Cargar datos"

Los nuevos equipos aparecen en el selector. Los puedes comparar con los que ya tenías.

---

## 🎯 Casos de Venta Reales

### **Caso 1: Licitación Educativa (IEP)**

**Contexto:**
- Colegio privado en Lima
- 45,000 páginas/mes (260 alumnos × 200 pág/mes)
- Funcionamiento: 8h/día, 22 días/mes
- Tarifa energía: $0.12/kWh (doméstica)

**Pasos:**
1. Volumen: 45,000
2. Horas: 8
3. Días: 22
4. Electricidad: 0.12
5. Selecciona: **Sharp BP-70M65A** vs **Ricoh MP C6502**

**Resultado esperado:**
- Sharp: ~$1,750/mes → $63,000 TCO 36m
- Ricoh: ~$1,950/mes → $70,200 TCO 36m
- **Ahorro Sharp: $7,200 en 3 años**

**Tu narrativa comercial:**
> "Con un volumen de 45k páginas/mes, Sharp es 11% más económico que Ricoh. En los 3 años del contrato, son $7,200 de ahorro garantizado. Sin contar que Sharp tiene voltaje estable, lo que significa menos riesgo de daño por fluctuaciones eléctricas en el colegio."

---

### **Caso 2: Industria de Packaging (HIGH VOLUME)**

**Contexto:**
- Empresa manufacturera
- 250,000 páginas/mes (reportes, etiquetas, documentación)
- Funcionamiento: 16h/día (2 turnos), 22 días/mes
- Tarifa energía: $0.18/kWh (zona industrial con picos)

**Pasos:**
1. Volumen: 250,000
2. Horas: 16 (16h × 22d = 352h/mes)
3. Días: 22
4. Electricidad: 0.18
5. Selecciona: **Sharp BP-70M65A**, **Kyocera TASKalfa 8580**, **RISO Valezus T2200**

**Resultado esperado:**
- Sharp: ~$5,200/mes → $187,200 TCO 36m
- Kyocera: ~$5,800/mes → $208,800 TCO 36m
- RISO: ~$4,200/mes → $151,200 TCO 36m ⭐
- **RISO gana porque consume 0.8kWh (vs 1.8-2.3 de otros)**

**Tu narrativa comercial:**
> "Con tarifa industrial a $0.18/kWh, la energía se convierte en el driver principal (no la renta). El RISO Valezus T2200 es 30% más barato que Sharp y 45% que Kyocera en 36 meses. Además, con 220ppm, da más que el doble de velocidad. Retorno garantizado."

---

### **Caso 3: Gobierno/Municipalidad (SENSIBILIDAD + ESCENARIOS)**

**Contexto:**
- Municipalidad de provincia
- Presupuesto ajustado
- Volumen estimado: 60,000 páginas/mes (pero INCIERTO)
- Riesgo: ¿Qué pasa si cae a 40,000?

**Pasos:**
1. Primero: Volumen 60,000 → Calcula
2. Luego: Volumen 40,000 → Recalcula
3. Compara Sharp vs Ricoh en ambos escenarios

**Resultado esperado:**
- **Escenario 1 (60k/mes):**
  - Sharp: $2,050/mes
  - Ricoh: $2,280/mes
  - Diferencia: $230/mes → $8,280 en 3 años

- **Escenario 2 (40k/mes):**
  - Sharp: $1,650/mes
  - Ricoh: $1,860/mes
  - Diferencia: $210/mes → $7,560 en 3 años

**Tu narrativa comercial:**
> "Incluso si baja el volumen 33%, Sharp sigue siendo la opción económica. No hay escenario donde Ricoh sea mejor. ¿Quieren certeza? Sharp es su garantía."

---

## 📊 Interpretación del Dashboard

### **KPI Cards (Arriba)**
Muestran:
- **Costo mensual** (grande, rojo/azul)
- **TCO 36 meses** (pequeño, verde)

**Lectura:** Si la tarjeta dice "$1,850/mes" + "$66,600 en 36m", el cliente paga $1,850 cada mes y acumula $66,600 en 3 años.

### **Desglose de Costos**
Cada equipo tiene 5 líneas:

```
Renta:        $850    (contrato mensual)
Costo/click:  $650    (volumen × 0.012 $/pág)
Papel:        $100    (volumen × 0.02 $/pág)
Energía:      $250    (horas × consumo × tarifa)
─────────────────
Total:        $1,850
```

**Uso comercial:** Si el cliente dice "pero el costo de papel es alto", puedes decir: "Ese costo es inevitable (es la ley de la física). Podemos optimizar renta o costo por click, pero papel siempre será ~$100/mes con este volumen."

### **Comparativa (Tabla TCO)**
Ordena de menor a mayor costo mensual. La fila verde (primera) es la ganadora.

**Lectura:** La diferencia entre mes 1 y mes 36 **se multiplica 36 veces**. Una diferencia de $100/mes = $3,600 en 3 años.

---

## 🎨 Tips para Cerrar Deals

### **Tip 1: Imprime/Exporta PDF**
- Desde tu navegador: `Ctrl+P` o `Cmd+P`
- Guardas como PDF
- Lo dejas con el cliente como "análisis técnico"

### **Tip 2: Haz "Sensibilidad"**
- Cambia volumen ±20%
- Muestra que Sharp sigue ganando
- Crea certeza en el cliente

### **Tip 3: Enfatiza el "Ahorro acumulado 36m"**
- "No es $200/mes"
- "Es $7,200 en los próximos 3 años"
- Los números grandes venden

### **Tip 4: Usa la recomendación automática**
Al final del Dashboard aparece:
> "El equipo más competitivo es Sharp BP-70M65A con $1,850 mensuales. Vs Ricoh: ahorro de $230/mes o $8,280 en 3 años."

**Cópialo y úsalo en tu email de seguimiento.**

---

## 📈 Qué Cambiar Según Vertical

| Vertical | Volumen | Horas | Días | Tarifa |
|----------|---------|-------|------|--------|
| **Educación (IEP)** | 30-80k | 8 | 22 | 0.12 |
| **Gobierno** | 40-100k | 8 | 22 | 0.13 |
| **Industria** | 100-300k | 16 | 22 | 0.18 |
| **Servicios (call center)** | 150-200k | 10 | 22 | 0.12 |
| **Print shops** | 200-500k | 16-20 | 22 | 0.14 |

---

## 🔧 Troubleshooting

### "No se ven los números"
→ Recarga la página (F5 / Cmd+R)

### "¿Cómo agrego más equipos?"
→ Click en "⬆ Importar", pega JSON, "Cargar datos"

### "¿Puedo comparar 10 equipos?"
→ Sí, pero recomendamos máx 5-6 para claridad. Selecciona los relevantes.

### "¿Los datos se guardan?"
→ No. La herramienta vive en tu navegador. Nada sube a internet. **Esto es una ventaja:** datos confidenciales.

### "¿Puedo usar mis precios reales?"
→ Sí, ese es el objetivo. Importa tu base de datos de equipos con tus rentas y costos.

---

## 💼 Workflow Recomendado

1. **Cliente envía TDR o especificación**
2. Tu abres TCO Pro
3. Pones volumen/energía del cliente
4. Importas equipos que ofreces (con tus precios)
5. Generas PDF del Dashboard
6. Envías email: "Análisis TCO 3 años: [PDF]"
7. **En la call:** "Mira la línea 36 meses... Sharp es $7,200 más barato que la alternativa"
8. **Cierre:** "¿Firmamos?"

---

## 📄 Ejemplo de Email Post-Análisis

---

**Asunto:** Análisis TCO Completo - Oportunidad de Ahorro $7,200

Estimado [Cliente],

Tras revisar tu requerimiento de 50,000 pág/mes, he corrido el análisis de Costo Total de Propiedad (TCO) en horizonte de 3 años.

**Resultado:** Sharp es 12% más económico que Ricoh.

**Desglose:**
- Sharp BP-70M65A: $1,850/mes → $66,600 en 36 meses
- Ricoh MP C6502: $2,080/mes → $74,880 en 36 meses
- **Tu ahorro: $8,280**

Adjunto análisis con desglose completo de renta, costo-por-click, papel y energía.

¿Podemos agendar 20 min esta semana para revisar la propuesta?

Saludos,
[Tu nombre]

---

## 🚀 Siguiente Paso

Personaliza los datos con **tus modelos, tus precios, tus márgenes**.

Exporta JSON de tu base de datos y importa.

**TCO Pro se convierte en tu vendedor más consistente.**

---

**¿Preguntas?** Las respuestas están en los números.
