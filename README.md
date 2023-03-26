# Creación de un modelo desde cero

[Clic](https://github.com/MenaVhs/DLC-Modelo) para instrucciones de instalación completa.

**[Documentación Oficial](https://deeplabcut.github.io/DeepLabCut/docs/standardDeepLabCut_UserGuide.html#b-configure-the-project)**

El presente trabajo fue realizado desde entorno virtual de DEEPLABCUT

## Creación del proyecto
```deeplabcut.create_new_project('CV', 'Mena', ['C:\Users\mena_\OneDrive - Centro de Enseñanza LANIA\Escritorio\DLC-Videos\Grupo1R3S15.mp4', 'C:\Users\mena_\OneDrive - Centro de Enseñanza LANIA\Escritorio\DLC-Videos\Grupo2R5S15.mp4'], working_directory='C:\Users\mena_\CV-Mena-2023-03-25', copy_videos=True, multianimal=False)```
<br>

Se crea el archivo config.yaml <br>
````config_path = r'C:\Users\mena_\CV-Mena-2023-03-25\config.yaml'```` <br>

Se agregan: bodyparts y el skeleton.
- crop=GUI

## Selección de datos
Desde la GUI, ver en Docs>img>Extrac Frames.png
````deeplabcut.extract_frames(config_path, mode='automatic', algo='kmeans', userfeedback=False, crop=GUI, cluster_step=3)````

## Etiquetado de frames
Ver en el [README](https://github.com/MenaVhs/DLC-Modelo) del proyecto DLC-Modelo cómo es el etiquetado en Napari.

## Entrenamiento




