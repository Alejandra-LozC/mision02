# PROMETHEUS · Coevaluación Misión 02

Aplicación web para coevaluación de equipos correspondiente a la Misión 02.

- El estudiante ingresa únicamente su ID.
- El sistema identifica automáticamente su equipo según la columna `mision02`.
- Solo aparecen sus compañeros de la Misión 02.
- No puede evaluarse a sí mismo.
- Rúbrica con pesos 25/20/20/20/15 % y descriptores conductuales por nivel.
- Se solicitan evidencias y una mejora opcional.
- Se indica que la evaluación debe basarse en conductas observables, no en afinidad.
- **Los resultados se guardan en `results_mision02.csv` dentro del repositorio de GitHub** usando la API de GitHub, lo que garantiza persistencia entre reinicios de la app.

## Configuración de GitHub

1. Crea un token clásico en GitHub con scope `repo`:
   **Settings → Developer settings → Personal access tokens → Tokens (classic) → Generate new token**.
2. En Streamlit Community Cloud, ve a **Settings → Secrets** y agrega:
   ```toml
   [github]
   token = "ghp_..."
   username = "tu_usuario"
   repo = "tu_repo"
   branch = "main"