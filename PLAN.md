# Plan de trabajo: clasificación de perros y gatos

## Alcance estricto del instructor

1. **Carga y comprensión del dataset**: localizar `dogs-vs-cats/train`, contar imágenes y mostrar nueve perros y nueve gatos en una figura.
2. **Preprocesamiento compatible con el hardware**: como el entorno tiene menos de 12 GB de RAM, no cargar las 25.000 imágenes en memoria; organizar el dataset en `train/test` y en subdirectorios `cat/dog`, usando `ImageDataGenerator.flow_from_directory()` con imágenes de `200x200`.
3. **Construcción de la RNA**: usar exactamente `EfficientNetB0(include_top=False, weights=None, input_shape=(224,224,3))`, `GlobalAveragePooling2D`, `Dense(128, relu)` y salida `Dense(2, softmax)`.
4. **Entrenamiento y evaluación**: compilar, entrenar, medir el rendimiento y representar la evolución del entrenamiento.
5. **Optimización solicitada**: utilizar `ModelCheckpoint` y `EarlyStopping` como callbacks, cargar el mejor modelo y predecir sobre test.
6. **Persistencia**: guardar el mejor modelo en `models/`.
7. **Verificación final**: comprobar cada punto del checklist, validar sintaxis/estructura y revisar que el repositorio solo incluya entregables del proyecto.
8. **Entrega Git**: crear commit, hacer push a una rama de trabajo y abrir un pull request hacia `main`.

## Fases de ejecución del agente

- **Fase 1 — Diagnóstico**: revisar instrucciones, estructura, hardware, dependencias y disponibilidad del dataset.
- **Fase 2 — Implementación**: completar el notebook reproducible con visualización, partición, generadores, modelo EfficientNet-B0, callbacks, evaluación y guardado.
- **Fase 3 — Validación**: verificar el checklist, imports, rutas, formas de entrada/salida y ausencia de errores evitables.
- **Fase 4 — Entrega**: revisar cambios, commit, push y creación del PR.

No se incorporan arquitecturas alternativas, aumentos de datos no solicitados, APIs web, despliegue ni análisis fuera de los puntos anteriores.
