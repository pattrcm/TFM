# Control interpretable de la identidad vocal en síntesis de voz

Trabajo de Fin de Máster (TFM) centrado en el análisis y control de atributos vocales (género, edad percibida y, como extensión, acento) mediante direcciones lineales en el espacio de condicionamiento de modelos TTS preentrenados, sin modificar ni reentrenar los pesos base.

## Alcance de esta fase (Bloque 1: Tareas 1–5)
- **Modelo base:** StyleTTS 2 (checkpoint preentrenado en LibriTTS, inglés), trabajando sobre el vector de estilo $z \in \mathbb{R}^{256}$ (mitad acústica y mitad prosódica).
- **Corpus:** VCTK, con partición estricta disjunta por locutor (`train` / `test`).
- **Objetivos cubiertos:** Hito de viabilidad, legibilidad mediante sondas lineales con validación cruzada por locutor, ortogonalización de direcciones y curvas frente a la intensidad $\alpha$.

## Estructura del repositorio
- `notebooks/`: Notebooks de experimentación en Kaggle.
- `resultados/hito_viabilidad/`: Audios `.wav` de prueba (voces base, interpolaciones y desplazamientos).
- `resultados/figuras/`: Gráficas y tablas generadas durante los experimentos.
