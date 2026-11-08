# Personal Coach Artifact

App personal de entrenamiento y nutrición de Daniel, construida como artefacto de Claude.

## Qué hace
- **Hoy:** registro de series (kg, reps, RIR y distancia) con lo que hiciste la última vez y una sugerencia de progresión.
- **Rutina:** programa *Hybrid Athlete & Calisthenics v2.0*, 100% editable (series, reps, carga, RIR, distancia, descanso).
- **Nutrición:** calorías y macros con Mifflin-St Jeor, calculados en código; menú del día con comparación ±5%.
- **Progreso:** check-in semanal, ajustes automáticos por reglas, gráficas de rendimiento y carga, kilómetros por sesión, peso y carga por ejercicio.
- **Perfil** y **Coach IA** (este último solo funciona dentro de claude.ai).
- Modo claro (blanco/azul) y oscuro (negro/naranja).

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
