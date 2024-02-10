# Suhora Internship Task - Data Analysis for Ship Detection with HRSID 

## Dataset
The initial step was to perform some basic visualizations to check how the annotations are mapped to the original images, then convert the COCO format to YOLO format for anootaions was carried out at `cocotoyolo.py`,  after which the data was split into train, test and validation sets, where the split ratio was 70%-train, 15%-test, 15%-validation at `Visualizations&DataSplit.ipynb`. The final step here was to crosscheck the annotation mapping with the images, so I did another round of visualization on the new format of annotations. 


## Training
For performing object detection, we set the `config.yaml` to the dataset paths, then utilize the pretrained ** YOLOv8 model** in `Tain.ipynb` to do this. The configurations for training this was the following:

- Training Epochs: `epochs=100`
- Input Image Size: `imgsz=800`
- Save Checkpoints: `save=True`
- Early Stopping Patience: `patience=10`
- Optimizer: `optimizer='Adam'`
- Initial Learning Rate: `lr0=0.001`
- Batch Size: `batch=8`

It took around 70 minutes to train the model where a single epoch took around 1:30 minutes, the early stopping callback triggered at the 42nd epoch where there was no improvement over the last 10 epochs, the best results were observed at epoch 31 with the map score being 0.905.


## Outputs
After training the model, the following are the results from some sample validation images :

![image](https://github.com/Maatrika-P/Ship-Detection-in-SAR-Images/assets/135828608/6b5e370e-549f-4e02-8201-95a93eab4038)


The following were the results from some sample training images:

![image](https://github.com/Maatrika-P/Ship-Detection-in-SAR-Images/assets/135828608/e97665a6-c930-479f-9486-3c7b91e351b6)
