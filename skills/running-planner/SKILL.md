# SKILL: Running Training Planner
**Versión:** 4.0 — Actualizada con datos reales de Strava (Mar 2026)  
**Metodología:** Maffetone (MAF) + 80/20 (Matt Fitzgerald / Seiler) + Periodización clásica  
**Creada para:** Adria — corredor de Barcelona

---

## CUÁNDO USAR ESTA SKILL

Usar esta skill cuando Adria pida:
- Generar o ajustar un plan de entrenamiento semanal
- Analizar datos de Strava o entrenamientos recientes
- Evaluar si un entrenamiento concreto fue correcto
- Recomendar sesiones específicas (series, long run, rodaje)
- Preparar un ciclo de carrera (media maratón, maratón)
- Calcular zonas de FC, ritmos objetivo o progresiones de volumen

---

## PERFIL DEL ATLETA

| Parámetro | Valor | Fuente |
|-----------|-------|--------|
| Nombre | Adria | — |
| Ciudad | Barcelona | — |
| Nivel | Intermedio (5-6 medias maratones completadas) | — |
| FC máxima real | **205 ppm** | Strava |
| FC media histórica global | **175.6 ppm** | Strava (154 runs, Sep 2023-Mar 2026) |
| FC habitual en carrera | 175-185 ppm | Strava |
| FC conversación posible hasta | ~170 ppm (umbral aeróbico elevado) | Observación directa |
| FC objetivo zona aeróbica | **150-158 ppm** (~73-77% FC máx) | Calculado |
| Ritmo actual a FC alta (~175 ppm) | 5:10-5:30 min/km | Strava |
| Ritmo actual a FC baja (155 ppm) | ~7:10 min/km | Primera sesión 29 Mar 2026 |
| Volumen semanal base real | **~20 km/semana** | Media últimas 8 semanas Strava |
| Días disponibles para running | 3 días/semana | — |
| Otros entrenamientos | Gimnasio 3 días/semana | — |
| Problema confirmado | **84.1% del tiempo en zona dura (>168 ppm). Solo 1.5% en zona fácil en 2.5 años.** | Strava |
| Estancamiento confirmado | Sin mejora de ritmo a FC similar en los últimos 10 meses | Strava |

### Zonas de FC reales (basadas en FC máx 205 ppm)

| Zona | % FC máx | Rango FC | Uso |
|------|----------|----------|-----|
| Z1 recuperación | 50-60% | 102-123 ppm | Recuperación activa |
| Z2 aeróbica base | 60-70% | 123-143 ppm | MAF estricto |
| Z3 zona gris | 70-80% | 143-164 ppm | Evitar en días fáciles |
| Z4 umbral | 80-90% | 164-184 ppm | Series, tempo |
| Z5 máximo | 90-100% | 184-205 ppm | Sprints, fin de carrera |

> Zona aeróbica práctica de Adria: **150-158 ppm** (entre Z3 alta y Z4 baja).
> Justificado por umbral aeróbico elevado confirmado. Más restrictivo no es más productivo para su perfil.

### Objetivos y calendario de carreras
| Fecha | Carrera | Objetivo |
|-------|---------|----------|
| Agosto 2026 | Media maratón | Test de progreso. Correr a 160-165 ppm controlado, sin atacar PR |
| Noviembre 2026 | Media maratón | **PR objetivo: 1:35-1:40 (4:30-4:44 min/km)** |
| Diciembre 2026 | Maratón | Terminar bien, objetivo ~5:00-5:10 min/km sin sufrir |

---

## PARTE 1 — CÓMO CALCULAR LAS ZONAS DE FC

### 1.1 Calcular la FC máxima real

La fórmula clásica (220 - edad) es poco fiable individualmente. Hay tres métodos, de menor a mayor precisión:

**Método A — Estimación por fórmula (menos preciso):**
```
FC máx estimada = 220 - edad
```
Para Adria a ~35 años → FC máx ≈ 185 ppm
⚠️ Poco fiable. Usar solo si no hay otro dato.

**Método B — Test de campo (más preciso):**
Correr 2 km al máximo esfuerzo después de calentamiento de 15 min.
El pico más alto registrado en el último km = FC máx real.
Mejor hacerlo en una carrera competitiva corta (5km o 10km).

**Método C — Datos de Strava (cuando estén disponibles):**
En el CSV de Strava, buscar el campo `max_heart_rate` en las actividades.
El valor más alto registrado en los últimos 12 meses = FC máx real.

> Para Adria: FC máx probable entre 188-195 ppm según su FC habitual de carrera.
> Actualizar cuando llegue el CSV de Strava.

---

### 1.2 Calcular la FC MAF (Maffetone)

La FC MAF es el techo de la zona aeróbica real. Fórmula base:

```
FC MAF = 180 - edad
```

Luego aplicar UNO de estos ajustes:

| Situación | Ajuste |
|-----------|--------|
| Enfermedad reciente, medicación, cirugía | -10 ppm |
| Lesionado, resfriados frecuentes, principiante, sin mejora reciente | -5 ppm |
| Entrena consistente 4x/semana sin problemas | +0 ppm |
| Entrena consistente 5x/semana más de 2 años sin lesiones | +5 ppm |

**Para Adria:**
- Lleva años corriendo pero con patrón de zona gris y sin mejora reciente → ajuste **-5**
- FC MAF teórico = 180 - 35 - 5 = **140 ppm**

> ⚠️ Excepción justificada para Adria: su umbral aeróbico real está elevado (puede hablar
> cómodamente a 170 ppm). Esto indica adaptación cardiovascular real aunque mal distribuida.
> Por eso se acepta **150-158 ppm** como zona aeróbica práctica, en lugar del 140 teórico
> que sería demasiado restrictivo y poco productivo para su nivel real.

**Regla del primer kilómetro:**
Siempre empezar 10 ppm por debajo del techo aeróbico.
Para Adria: primeros 10-15 min de cualquier sesión por debajo de **148 ppm**.

---

### 1.3 Calcular las 5 zonas de FC

Una vez conocida la FC máxima real, calcular zonas así:

```
Zona 1 (recuperación):    50-60% FC máx
Zona 2 (aeróbica base):   60-70% FC máx  ← donde deben ir los rodajes suaves
Zona 3 (aeróbica alta):   70-80% FC máx  ← "zona gris", evitar en días fáciles
Zona 4 (umbral):          80-90% FC máx  ← series y tempo
Zona 5 (máximo):          90-100% FC máx ← sprints, final de carrera
```

**Para Adria (con FC máx estimada 190 ppm):**

| Zona | % FC máx | Rango FC | Uso |
|------|----------|----------|-----|
| Z1 | 50-60% | 95-114 ppm | Recuperación activa |
| Z2 | 60-70% | 114-133 ppm | Aeróbica base (MAF estricto) |
| Z3 | 70-80% | 133-152 ppm | Zona gris — evitar en días fáciles |
| Z4 | 80-90% | 152-171 ppm | Umbral, tempo, series largas |
| Z5 | 90-100% | 171-190 ppm | Series cortas, fin de carrera |

> La zona aeróbica práctica de Adria (150-158 ppm) cae entre Z3 alta y Z4 baja.
> Actualizar estas zonas con FC máx real del CSV de Strava.

---

### 1.4 Fórmula de Karvonen (cálculo más preciso)

Usa la FC de reserva (diferencia entre FC máx y FC en reposo):

```
FC entrenamiento = ((FC máx - FC reposo) × % intensidad) + FC reposo
```

**Ejemplo para Adria** (FC máx 190, FC reposo 52):
- FC reserva = 190 - 52 = 138 ppm
- Zona aeróbica al 65%: (138 × 0.65) + 52 = **141 ppm**
- Zona aeróbica al 75%: (138 × 0.75) + 52 = **155 ppm**

Para aplicar Karvonen: medir FC reposo al despertar, tumbado, antes de levantarse.
Hacerlo 3 días seguidos y hacer la media.

---

## PARTE 2 — CÓMO CALCULAR RITMOS OBJETIVO

### 2.1 Calcular ritmo objetivo desde tiempo meta

```
Ritmo (min/km) = Tiempo objetivo en minutos / Distancia en km
```

**Ejemplos para Adria:**

| Carrera | Tiempo objetivo | Ritmo resultante |
|---------|----------------|------------------|
| Media maratón | 1:35:00 | 95 / 21.097 = **4:30 min/km** |
| Media maratón | 1:40:00 | 100 / 21.097 = **4:44 min/km** |
| Maratón | 3:30:00 | 210 / 42.195 = **4:58 min/km** |
| Maratón | 3:45:00 | 225 / 42.195 = **5:20 min/km** |

---

### 2.2 Estimar el potencial real desde rendimiento actual

Si Adria corre 21 km a 5:15 min/km (~1:50:30) con FC 175-185:
- Con base aeróbica bien desarrollada (6 meses de trabajo correcto), el potencial real es:
  - Media maratón: **1:35-1:40**
  - Maratón: **3:30-3:45**

Esto confirma que el objetivo de 1:35-1:40 en noviembre es ambicioso pero alcanzable.

---

### 2.3 Calcular ritmos de entrenamiento derivados del ritmo objetivo

A partir del ritmo objetivo de media (4:44 min/km como referencia):

| Tipo de sesión | Offset sobre ritmo media | Ritmo concreto |
|----------------|--------------------------|----------------|
| Long run aeróbico | +90 a +120 seg/km | 6:14 - 6:44 min/km |
| Rodaje suave | +60 a +90 seg/km | 5:44 - 6:14 min/km |
| Tempo / umbral | -5 a +10 seg/km | 4:39 - 4:54 min/km |
| Series 1 km | -15 a -25 seg/km | 4:19 - 4:29 min/km |
| Series 400m | -30 a -40 seg/km | 4:04 - 4:14 min/km |

> Ahora mismo Adria va a 7:11 en rodaje suave → está bien, es coherente con fase inicial.
> A medida que mejore la base aeróbica, ese ritmo bajará progresivamente manteniendo la misma FC.

---

## PARTE 3 — CÓMO CALCULAR LA PROGRESIÓN DE VOLUMEN

### 3.1 Regla del 10%

Nunca aumentar el volumen semanal total más de un 10% respecto a la semana anterior:

```
Volumen semana N+1 ≤ Volumen semana N × 1.10
```

**Ejemplo:**
- Semana 1: 32 km → Semana 2 máximo: 35 km
- Semana 2: 35 km → Semana 3 máximo: 38 km

---

### 3.2 Ciclo de carga 3:1

La progresión debe seguir ciclos de **3 semanas de carga + 1 semana de recuperación**:

```
Semana 1: volumen base       → ej. 35 km
Semana 2: +10%               → ej. 38 km
Semana 3: +10% sobre sem. 1  → ej. 40 km  (NO sobre semana 2)
Semana 4: RECUPERACIÓN       → bajar al 60-70% de semana 3 → 24-28 km
Semana 5: retomar desde sem. 3 y continuar subiendo
```

En semana de recuperación: misma estructura (3 días running), sesiones más cortas.
Long run baja a 50-60 min. Series con menos volumen (ej. 5x400 en vez de 8x400).

---

### 3.3 Volumen máximo sostenible para Adria

Con 3 días de running + gimnasio 3 días:
- Volumen sostenible largo plazo: **40-50 km/semana**
- Volumen pico en fase específica (2-3 semanas puntuales): hasta **55 km/semana**
- No superar este techo para evitar sobreentrenamiento combinado con el trabajo de gimnasio

---

### 3.4 Progresión del long run

| Fase | Duración long run | Distancia aprox a 7:00/km |
|------|-------------------|---------------------------|
| Inicio (ahora) | 1h20-1h30 | 11-13 km |
| Base consolidada (mes 2-3) | 1h40-1h50 | 14-16 km |
| Específica media (mes 4-5) | 1h50-2h00 | 16-18 km |
| Específica maratón (mes 6) | 2h00-2h30 | 17-21 km |

Nunca superar 2h30 en un long run. Más tiempo no aporta beneficio proporcional y aumenta riesgo de lesión.

---

## PARTE 4 — CÓMO DISEÑAR LAS SERIES

### 4.1 Principios básicos

- Volumen de series (metros totales a ritmo fuerte) no debe superar el **8-10% del volumen semanal total**
- Calentamiento mínimo de 15 min antes de cualquier sesión de calidad
- Enfriamiento mínimo de 10 min después
- Si el ritmo baja más de 5 seg/km en la siguiente serie → recuperación insuficiente o ritmo demasiado alto
- Nunca terminar las series "vacío". Mejor hacer una menos que forzar la última mal

### 4.2 Tipos de series según fase

**Series cortas 200-400m → potencia neuromuscular (fase BASE):**
- Ritmo: 4:00-4:15 min/km
- Recuperación: 2-3 min andando o trote muy suave
- Volumen: 6-10 repeticiones
- Objetivo: mantener velocidad neuromuscular mientras se construye la base aeróbica

**Series medias 800m-1km → umbral de velocidad (fase ESPECÍFICA):**
- Ritmo: 4:20-4:35 min/km
- Recuperación: 90 seg - 2 min trote suave
- Volumen: 5-8 repeticiones

**Series largas 1 milla / 2km → umbral láctico (fase RACE-PREP):**
- Ritmo: 4:40-4:50 min/km (cerca del ritmo objetivo de media)
- Recuperación: 3 min trote suave
- Volumen: 3-5 repeticiones

**Tempo run continuo → umbral láctico sostenido (fase ESPECÍFICA):**
- Ritmo: 4:44-5:00 min/km durante 20-35 min sin parar
- Test de intensidad correcta: "puedo hablar pero con esfuerzo, frases muy cortas"
- No confundir con rodaje: el tempo debe incomodar

**Fartlek → velocidad libre (cualquier fase):**
- Formato básico: 10 x (1 min rápido / 1 min suave)
- Minutos rápidos a sensación fuerte (~4:20-4:30), suaves a ~6:30-7:00
- Bueno cuando no se quiere presión de ritmo exacto

---

## PARTE 5 — CÓMO INTERPRETAR EL CSV DE STRAVA

Cuando Adria aporte el CSV de Strava, analizar estos campos:

### Campos clave
| Campo CSV | Qué extraer |
|-----------|-------------|
| `Average Heart Rate` | FC media de cada sesión |
| `Max Heart Rate` | Para calcular FC máx real |
| `Average Pace` | Ritmo medio por actividad |
| `Distance` | Distancia por sesión |
| `Moving Time` | Duración real |
| `Activity Type` | Filtrar solo actividades "Run" |

### Análisis a realizar

**1. FC máxima real:**
Buscar el valor más alto en `Max Heart Rate` de los últimos 12 meses.
Usar ese valor para recalcular todas las zonas (ver Parte 1.1).

**2. Distribución de FC histórica:**
Calcular qué % de sesiones tienen FC media por encima de 165 ppm.
Si >60% → confirma patrón de zona gris y justifica el cambio de metodología.

**3. Volumen semanal real:**
Agrupar actividades por semana, sumar distancias.
Media de las últimas 8 semanas = volumen base real de Adria.
Usar ese dato como punto de partida de la progresión.

**4. Correlación ritmo-FC:**
Buscar sesiones similares en distancia y comparar FC media con ritmo medio.
Si FC sube pero ritmo no mejora entre sesiones → fatiga acumulada o sobreentrenamiento.

**5. Progresión histórica:**
Ver si el ritmo medio en sesiones de duración similar ha mejorado, empeorado o se ha
estancado en los últimos 6-12 meses. Si se ha estancado → confirma zona gris crónica.

**6. Ratio fácil/duro real:**
Clasificar sesiones por FC media:
- FC media < 158 ppm → sesión fácil (aeróbica)
- FC media 158-168 ppm → zona gris
- FC media > 168 ppm → sesión dura

Calcular % de cada categoría. Objetivo futuro: ~80% fácil / 20% duro.

### Ajustes tras analizar Strava
- Si FC máx real > 192 → subir el techo de zona aeróbica práctica a 160-163 ppm
- Si FC máx real < 185 → bajar el techo de zona aeróbica práctica a 148-153 ppm
- Si volumen base < 28 km/semana → empezar progresión más conservadora (no superar 30 km semana 1)
- Si hay muchas semanas irregulares (saltos grandes de volumen) → priorizar consistencia 8 semanas antes de subir intensidad

---

## PARTE 6 — CÓMO DETECTAR Y GESTIONAR EL SOBREENTRENAMIENTO

### Señales de alarma
- FC en reposo sube más de 5-7 ppm sobre la habitual (medir cada mañana al despertar)
- El ritmo habitual se vuelve más difícil a la misma FC
- Piernas cargadas más de 2 días seguidos
- Sueño perturbado o sensación de no recuperar aunque se duerma bien
- Irritabilidad o falta de motivación para entrenar
- Más resfriados o infecciones de lo habitual

### Protocolo de ajuste si aparecen 2 o más señales
1. Cancelar la sesión de calidad esa semana
2. Solo rodajes suaves a FC < 150 ppm durante 5-7 días
3. Si persiste después de una semana → tomar 3-5 días de descanso total
4. Retomar con semana de recuperación (60% del volumen habitual)

### Cuándo insertar semana de recuperación extra (además del ciclo 3:1)
- Después de cualquier carrera (mínimo 1 semana muy suave)
- Si se encadenan 4 semanas de carga sin recuperación por cualquier motivo
- Si FC reposo elevada más de 3 días seguidos
- En momentos de alto estrés laboral o personal (el cuerpo no distingue el origen del estrés)

---

## PARTE 7 — ESTRUCTURA SEMANAL DETALLADA

### Semana tipo estándar

```
LUNES     → Gimnasio (fuerza)
MARTES    → Rodaje aeróbico suave [45-60 min @ 148-155 ppm]
MIÉRCOLES → Gimnasio (fuerza)
JUEVES    → Sesión de calidad [series / tempo / fartlek]
VIERNES   → Gimnasio (fuerza)
SÁBADO    → Long run aeróbico [1h20-1h40 @ 150-158 ppm]
DOMINGO   → Descanso total
```

### Semana de recuperación (cada 4ª semana)

```
LUNES     → Gimnasio (carga reducida)
MARTES    → Rodaje suave [35-40 min @ <150 ppm]
MIÉRCOLES → Gimnasio (carga reducida)
JUEVES    → Series cortas ligeras [5x400m o fartlek suave 20 min]
VIERNES   → Gimnasio (carga reducida)
SÁBADO    → Long run corto [50-60 min @ <155 ppm]
DOMINGO   → Descanso total
```

### Semana de taper (race week y semana anterior)

```
Semana -2:
  Martes   → Rodaje suave 40 min @ <152 ppm
  Jueves   → Series cortas: 5x400m con recuperación completa
  Sábado   → Long run reducido: 60-70 min @ <155 ppm

Semana -1 (race week):
  Martes   → Rodaje suave 25-30 min @ <150 ppm
  Jueves   → 4-5 strides de 20 seg a ritmo de carrera + 15 min suave total
  Viernes  → Descanso
  Sábado   → 20 min muy suave @ <150 ppm
  Domingo  → CARRERA
```

---

## PARTE 8 — PERIODIZACIÓN COMPLETA ADRIA 2026

### FASE 1 — BASE AERÓBICA (Abril → Julio, ~16 semanas)
- **Foco:** Construir motor aeróbico. Es la fase más importante del ciclo.
- 80% del volumen a 148-158 ppm
- Series en formato corto (400m) para mantener velocidad neuromuscular
- No mirar el ritmo del long run. Solo controlar la FC.
- Volumen semanal: 30 km → 45 km con ciclos 3:1
- MAF test cada 4-6 semanas para medir progreso real

### FASE 2 — TEST (Agosto)
- Carrera de media maratón como test real de forma
- **Estrategia:** Salir a 160-165 ppm y mantener constante todo el recorrido. No mirar el ritmo.
- Anotar ritmo resultante y comparar con misma FC en entrenamientos
- Objetivo: evaluar mejora, no PR
- Post-carrera: 1 semana de recuperación completa

### FASE 3 — ESPECÍFICA MEDIA (Septiembre → Octubre, ~8 semanas)
- **Foco:** Trabajo a ritmo objetivo (4:44 min/km o el ajustado tras el test de agosto)
- Introducir tempo runs (20-25 min a ritmo de media)
- Long run con últimos 20-30 min a ritmo objetivo
- Volumen: 35-45 km/semana
- Series medias y largas (800m, 1km, 1 milla)

### FASE 4 — PICO Y TAPER MEDIA (Noviembre, ~3 semanas antes)
- Semana -3: Última semana de carga alta (volumen pico del ciclo)
- Semana -2: Reducir volumen 30%, mantener una sesión de calidad corta
- Semana -1 (race week): Solo rodajes suaves + strides el jueves

### FASE 5 — TRANSICIÓN A MARATÓN (Noviembre-Diciembre)
- 1 semana de recuperación post-media antes de retomar
- Long runs progresivos hacia 2h-2h15 a FC aeróbica (150-158 ppm)
- No es ciclo de máximo rendimiento: es consolidación y resistencia
- Ritmo objetivo maratón: 5:00-5:10 min/km
- Estrategia de carrera: salir los primeros 25 km a 5:10, soltar si hay buenas sensaciones

---

## PARTE 9 — MAF TEST (MEDICIÓN DE PROGRESO)

### Cómo hacer el MAF test
1. Elegir un recorrido plano de 5-6 km. **Siempre el mismo.**
2. Calentar 15 min a FC < 148 ppm
3. Correr los 5-6 km manteniendo FC lo más constante posible en **155 ppm**
4. Registrar el ritmo medio resultante
5. Repetir cada 4-6 semanas en las mismas condiciones (hora del día, temperatura, descansado)

### Tabla de progreso esperado para Adria
| Semana | FC test | Ritmo esperado |
|--------|---------|----------------|
| 1-4 | 155 ppm | ~7:10-7:20 min/km |
| 6-8 | 155 ppm | ~6:50-7:00 min/km |
| 10-12 | 155 ppm | ~6:30-6:45 min/km |
| 16-18 | 155 ppm | ~6:10-6:25 min/km |
| 22-24 | 155 ppm | ~5:50-6:10 min/km |

### Si después de 8 semanas el ritmo no mejora, revisar en este orden:
1. ¿Se está respetando la FC baja en los rodajes? (causa más frecuente)
2. ¿Hay suficiente sueño (7-8h por noche)?
3. ¿La nutrición es adecuada (carbohidratos suficientes antes/después de entrenar)?
4. ¿Hay estrés elevado externo (laboral, personal)?
5. ¿El volumen semanal total es suficiente para generar adaptación?

---

## PARTE 10 — AJUSTES POR TEMPERATURA Y CLIMA (BARCELONA)

### Por qué la temperatura afecta al entrenamiento

El calor obliga al corazón a trabajar más para enfriar el cuerpo mediante sudoración y vasodilatación periférica, además de para mover los músculos. A mayor temperatura, mayor FC para la misma intensidad percibida. Ignorar esto lleva a interpretar mal los datos y a entrenar en zona gris sin saberlo.

**Efecto cuantificado:**
- Por cada 5°C por encima de 20°C → la FC sube aproximadamente 3-5 ppm a mismo esfuerzo
- A 30°C (verano Barcelona), la FC puede ser 10-15 ppm más alta que a 15°C a idéntica intensidad
- La humedad agrava el efecto: a 30°C con 70% humedad el impacto es mayor que a 30°C con 40%

---

### Ajuste de techo de FC por temperatura

| Temperatura | Ajuste sobre techo habitual (158 ppm) | Techo ajustado para Adria |
|-------------|---------------------------------------|---------------------------|
| < 15°C | +0 ppm | 158 ppm |
| 15-20°C | +0 ppm | 158 ppm |
| 20-25°C | -3 ppm | 155 ppm |
| 25-30°C | -6 ppm | 152 ppm |
| > 30°C | -10 ppm | 148 ppm |

> En días de calor extremo (>32°C), priorizar siempre la sensación de esfuerzo sobre el número exacto.
> Si a 148 ppm el esfuerzo ya se siente alto → bajar más el ritmo o acortar la sesión.

---

### Ajuste de ritmo esperado por temperatura

En verano los ritmos serán más lentos a la misma FC. Esto es correcto y esperado, no es un retroceso.

| Temperatura | Penalización de ritmo aproximada |
|-------------|----------------------------------|
| < 20°C | 0 seg/km |
| 20-25°C | +15-20 seg/km |
| 25-30°C | +25-35 seg/km |
| > 30°C | +40-60 seg/km |

**Ejemplo para Adria:**
- A 15°C corre a 7:10 min/km a 155 ppm → normal
- A 28°C el mismo esfuerzo aeróbico puede requerir ir a 7:45-8:00 min/km → también normal

---

### Franjas horarias recomendadas en Barcelona

| Mes | Temperatura habitual | Franja recomendada |
|-----|---------------------|--------------------|
| Abril - Mayo | 15-22°C | Cualquier hora |
| Junio | 20-28°C | Antes de las 9h o después de las 20h |
| Julio - Agosto | 25-35°C | Antes de las 8h o después de las 21h |
| Septiembre | 20-27°C | Antes de las 9h o después de las 20h |
| Octubre - Marzo | 10-18°C | Cualquier hora |

> El long run del sábado en julio y agosto debe hacerse muy temprano (7:00-7:30h).
> Entrenar a mediodía en verano en Barcelona invalida el objetivo de FC baja.

---

### El MAF test en verano: cómo interpretarlo correctamente

El MAF test **no debe compararse directamente** entre invierno y verano. Un ritmo peor en agosto respecto a abril no significa regresión si la temperatura es mucho más alta.

**Protocolo para comparar correctamente:**
- Intentar hacer siempre el MAF test en condiciones similares (misma franja horaria, temperatura parecida)
- Si no es posible, anotar la temperatura y humedad junto al resultado
- Comparar solo tests hechos en condiciones similares (±3°C)
- Un ritmo de 7:00 min/km a 155 ppm con 16°C equivale aproximadamente a 7:30-7:40 min/km con 28°C

---

### Hidratación y su efecto en la FC

La deshidratación sube la FC aunque la intensidad sea la misma, porque el corazón debe latir más veces para compensar la reducción de volumen sanguíneo.

**Reglas básicas:**
- Beber 400-500 ml de agua en las 2 horas previas a entrenar
- En sesiones > 60 min con calor: llevar agua o planificar fuente en el recorrido
- En sesiones > 90 min con calor: considerar bebida con electrolitos (sodio, potasio)
- Si la FC en el MAF test está 5-8 ppm más alta de lo esperado → revisar hidratación antes de concluir que hay regresión

**Señal de deshidratación durante el entrenamiento:**
FC sube progresivamente aunque el ritmo sea constante (fenómeno llamado "cardiac drift").
Si en el último tercio del long run la FC sube más de 8-10 ppm sin subir el ritmo → deshidratación.
Solución inmediata: bajar el ritmo y beber.

---

### Aclimatación al calor

El cuerpo tarda entre **10 y 14 días** en adaptarse a entrenar con calor. Durante ese período:
- La FC será más alta de lo normal para el mismo esfuerzo
- La sensación de esfuerzo será mayor
- El rendimiento bajará temporalmente

**Esto ocurre cada año al inicio del verano**, aunque se haya entrenado con calor el año anterior.
No interpretar los primeros 2 semanas de junio como regresión.

Después de la aclimatación, el cuerpo mejora:
- Mayor volumen de plasma sanguíneo
- Sudoración más eficiente (empieza antes, más distribuida)
- FC más baja para el mismo esfuerzo en calor

---

### Implicaciones para el calendario de Adria

| Período | Situación climática Barcelona | Implicación para el entrenamiento |
|---------|-------------------------------|-----------------------------------|
| Abril-Mayo | Fresco, ideal | Aprovechar para establecer ritmos de referencia en MAF test |
| Junio-Julio | Calor creciente | Ajustar FC y ritmos. Entrenar temprano. No comparar con primavera. |
| Agosto | Calor máximo | Carrera test con ajuste de expectativas. Salir conservador. |
| Septiembre | Calor moderado bajando | Transición a fase específica. Ritmos mejorarán al bajar temperatura. |
| Octubre-Noviembre | Fresco, ideal para PR | Condiciones óptimas para la media maratón objetivo. |

> La media de noviembre coincide con las mejores condiciones climáticas del año en Barcelona.
> Esto es una ventaja real: el cuerpo habrá entrenado todo el verano con handicap térmico
> y en noviembre rendirá mejor de lo que los entrenamientos estivales sugerían.

---

## REGLAS DE ORO

1. **La FC manda, no el ritmo.** Si hay que caminar en cuesta para no pasar de 158 ppm, se camina.
2. **Nunca dos días de running seguidos** con la estructura actual de 3 días.
3. **Los días fáciles deben ser fáciles de verdad.** Martes a 170 ppm = entrenamiento inútil.
4. **El progreso se mide en ritmo a FC constante**, no en ritmo absoluto.
5. **Ciclos 3:1 siempre.** Tres semanas de carga, una de recuperación.
6. **Nunca aumentar volumen más del 10% semanal.**
7. **Consistencia > heroísmo.** Un entrenamiento mediocre hecho vence a uno perfecto no hecho.
8. **Calentamiento obligatorio.** Primeros 10-15 min de cualquier sesión por debajo de 148 ppm.
9. **El gimnasio complementa.** La fuerza reduce lesiones y mejora la economía de carrera.
10. **Después de cada carrera, mínimo 1 semana de recuperación completa.**

---

*Skill v4.0 — Marzo 2026. Zonas de FC actualizadas con datos reales de Strava (154 runs, Sep 2023 - Mar 2026). FC máx real: 205 ppm. Volumen base: ~20 km/semana.*
