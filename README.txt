If you run the fetch_dataset.py script, it will download all the available images and place them to the different folders (train_set and test_set). Also, the script will move the annotations to the regarding folders. Please note that downloading process takes some time. Your folder should look like below before running the script.

BAFMD Dataset Folder
│   BAFMD_image_urls.tsv
│   BAFMD_train_images.txt    
│   BAFMD_test_images.txt
|   fetch_dataset.py
└───annotations
│    │   image1.jpg
│    │   image1.txt
│    |   image1.xml
│    │   image2.jpg
│    │   .
│    │   .


----------------

There are two different annotation files for each image. Both annotation files have the same bounding boxes. Regarding your label format, you can choose the one that you will use.

1-) image_name.txt annotation that uses YOLO labeling format which is object class, object coordinates, height, and width. All of them are normalized between 0 and 1

2-) image_name.xml annotation that uses Pascal VOC labeling format. It contains image size, object coordinates and class names.