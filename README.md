# Creación de un modelo desde cero

[Clic](https://github.com/MenaVhs/DLC-Modelo) para instrucciones de instalación completa.

**[Documentación Oficial](https://deeplabcut.github.io/DeepLabCut/docs/standardDeepLabCut_UserGuide.html#b-configure-the-project)**

El presente trabajo fue realizado desde entorno virtual de DEEPLABCUT

## Creación del proyecto
```deeplabcut.create_new_project('CV', 'Mena', ['C:\Users\...\Grupo1R5S15.mp4', 'C:\Users\...\Grupo2R5S15.mp4'], working_directory='C:\Users\mena_\CV-Mena-2023-03-25', copy_videos=True, multianimal=False)```
<br>

Se crea el archivo config.yaml <br>
````config_path = r'C:\Users\mena_\CV-Mena-2023-03-25\config.yaml'```` <br>


## Selección de datos
Desde la GUI, ver en Docs>img>Extrac Frames.png
````deeplabcut.extract_frames(config_path, mode='automatic', algo='kmeans', userfeedback=False, crop=GUI, cluster_step=3)````

## Etiquetado de frames
Ver en el [README](https://github.com/MenaVhs/DLC-Modelo) del proyecto DLC-Modelo cómo es el etiquetado en Napari.

## Creación del dataset 
```deeplabcut.generate_training_dataset.trainingsetmanipulation.create_training_dataset(config_path, num_shuffles=1, Shuffles=None, net_type='resnet_101', augmenter_type='imgaug')```

## Entrenamiento
```deeplabcut.pose_estimation_tensorflow.training.train_network(config_path, shuffle=1, trainingsetindex=0, gputouse=0, max_snapshots_to_keep=200000, autotune=True, displayiters=1000, saveiters=1000, maxiters=250000, allow_growth=True, keepdeconvweights=True)```
<!-- Inicio de entrenamiento de iteración 0: 26/03/2023, 2:55 p.m. Hora de fin: 9:01:00 p.m. 
En la iteración 229000; loss: 0.171%; lr: 0.02-->

## Exportar el modelo entrenado
```deeplabcut.export_model(config_path, iteration=None, shuffle=1, trainingsetindex=0,snapshotindex='all', TFGPUinference=True, overwrite=False, make_tar=True)```
