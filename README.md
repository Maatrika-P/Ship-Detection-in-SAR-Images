# Suhora Internship Task - Data Analysis for Ship Detection with HRSID 

## Dataset
The initial step was to perform some basic visualizations to check how the annotations are mapped to the original images, then convert the COCO format to YOLO format for anootaions was carried out at `cocotoyolo.py`,  after which the data was split into train, test and validation sets, where the split ratio was 70%-train, 15%-test, 15%-validation at `Visualizations&DataSplit.ipynb`. The final step here was to crosscheck the annotation mapping with the images, so I did another round of visualization on the new format of annotations. 
