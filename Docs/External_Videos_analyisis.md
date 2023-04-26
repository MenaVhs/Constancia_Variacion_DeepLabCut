## Proyecto Open_Fiel_6030
video_path =  r'C:\Users\Pc-Ryzen\Desktop\Constancia_Variacion_DeepLabCut\Videos\Open_Fiel_6030\R70_V2_D_F4.mp4'

## Proyecto en ADFE
video_path =  r'C:\Users\Pc-Ryzen\Desktop\Constancia_Variacion_DeepLabCut\Videos\ADFE\GrupoTCRata6Fase3PM2.mp4'

## Proyecto en Shoenfeld 
video_path =  r'C:\Users\Pc-Ryzen\Desktop\Constancia_Variacion_DeepLabCut\Videos\Schoenfeld\Grupo2R5S15.mp4'

### Análisis de videos nuevos
Relativos: <br>
````deeplabcut.analyze_videos(config_path, video_path , videotype='mp4', shuffle=1, trainingsetindex=0, gputouse=0, save_as_csv=True, destfolder=None, dynamic=(True, .5, 10))````<br>
Absolutos:<br>
````deeplabcut.analyze_videos(config_path, video_path , videotype='mp4', shuffle=1, trainingsetindex=0, gputouse=0, save_as_csv=True)````

### Filtrado
````deeplabcut.filterpredictions(config_path, video_path, shuffle=1, videotype='mp4', trainingsetindex=0, filtertype='arima', p_bound=0.01, ARdegree=5, MAdegree=2, alpha=0.01)````

### Graficar
````deeplabcut.plot_trajectories(config_path, video_path, videotype='.mp4', shuffle=1, imagetype='.png', resolution=100, linewidth=1.0)````<br>
````deeplabcut.utils.plotting.plot_trajectories(config_path, video_path, videotype='mp4', shuffle=1, trainingsetindex=0, displayedbodyparts='all', displayedindividuals='all', showfigures=False, imagetype='.png', resolution=100, linewidth=1.0)````
deeplabcut.utils.plotting.plot_trajectories(config_path, video_path, videotype='mp4')

### Crear videos etiquetados
````deeplabcut.create_labeled_video(config_path,video_path, videotype='.mp4', keypoints_only=True)````<br>
(Información para crear videos etiquetados)[https://deeplabcut.github.io/DeepLabCut/docs/standardDeepLabCut_UserGuide.html#extract-skeleton-features]<br>
**NEW** as of 2.2b8: You can create a video with only the “dots” plotted, i.e., in the style of Johansson, by passing keypoints_only=True:
