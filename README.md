# Personal Coach Artifact

App personal de entrenamiento y nutrición de Daniel, construida como artefacto de Claude.

## Qué hace
- **Hoy:** registro de series (kg, reps, RIR y distancia) con lo que hiciste la última vez y una sugerencia de progresión.
- **Rutina:** programa *Hybrid Athlete & Calisthenics v2.0* organizado en Calentamiento, Entrenamiento y Enfriamiento; 100% editable.
- **Nutrición:** calorías y macros con Mifflin-St Jeor, calculados en código; menú del día con comparación ±5%.
- **Progreso:** check-in semanal, ajustes automáticos por reglas, gráficas de rendimiento y carga, kilómetros por sesión, peso y carga por ejercicio.
- **Perfil** y **Coach IA** (este último solo funciona dentro de claude.ai).
- Modo claro (blanco/azul) y oscuro (negro/naranja).

## Guía rápida

**Tu semana en 4 pasos**
1. **Una vez:** llena *Perfil* (edad, estatura, peso, objetivo, equipo, lesiones, alimentos).
2. **Cada entreno:** abre *Hoy*, palomea el calentamiento, registra cada serie del entrenamiento (reps, kg, distancia y RIR), palomea el enfriamiento y toca **Guardar sesión**.
3. **Cada semana:** haz el check-in en *Progreso* y aplica los ajustes sugeridos.
4. **Cuando quieras:** pregúntale al *Coach IA* (solo dentro de claude.ai).

**Estructura de cada día (Rutina):** Calentamiento (checklist) · Entrenamiento en bloques (series, reps, carga, distancia + unidad, RIR objetivo, descanso; se registra serie por serie en *Hoy*) · Enfriamiento (checklist). Se edita con **Editar día**.

**Progresión**
- Fuerza: doble progresión. Tope del rango en todas las series con RIR ≥ objetivo → +1.25–2.5 kg.
- Carries: distancia completa en todas las series → +2.5–5 kg.
- Carrera: +5–10% por semana; cada 4ª semana repite o baja.

**Reglas automáticas del check-in**
- Peso sin moverse 2 semanas con adherencia ≥ 80% → ±150 kcal.
- Energía o sueño < 5 → −20% de series del entrenamiento.
- 3 sesiones sin superar tu mejor serie → cambia esquema o ejercicio.
- Notas con "dolor agudo" o "mareo" → aviso médico y pausa de subidas de carga.

**Nutrición:** Mifflin-St Jeor × factor de actividad ± déficit/superávit; proteína y grasa por kg y carbohidratos con el resto.

La guía completa está en la pestaña **Guía** de la app.

## Archivos
| Archivo | Para qué |
|---|---|
| `index.html` | Versión independiente: ábrela en cualquier navegador. Guarda tus datos en ese navegador (sin nube ni Coach IA). |
| `src/coach-artifact.html` | Código fuente exacto del artefacto publicado en claude.ai (Claude le agrega el `<html>`/`<head>` al publicar). |

## Uso local
Doble clic en `index.html`, o:
```bash
python3 -m http.server 8000   # luego abre http://localhost:8000
```

## Datos personales
Este repo es **público**: no subas aquí el respaldo JSON (Perfil → Copiar respaldo). Guárdalo en un repo privado o en `backups/`, que está en `.gitignore`.
