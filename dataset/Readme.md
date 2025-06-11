<h3>Dataset file Structure</h3>
Here in data set folder we need further two directories as images and labels.

Images containse two directories of train and val which is used to place training images and validation images respectively.

Labels directories contains all the labels we annotated for training and validation images from makesense.ai.

In dataset.yaml file we place the paths for the Project directory,Images directory and Labels directory. We give the values for the object based the order we annotated in makesense.ai. And we train the model by opening the terminal from the project directory
and executing the command-

    yolo task=detect mode=train model=yolov8n.pt data=dataset.yaml epochs=50 imgsz=640

from above command it trains the yolo model with the data we given.

NOTE:-We can use the any of the yolo versions-"nano,medium,small,large and extra large"

To view the object detection in live webcam we need to use the command:-

    yolo task=detect mode=predict model=best.pt source=0,1,2 show=True

You can change the source depending on the cam you are using, and if you want to predict on images then you give the directory/image path.
NOTE:-If you are outside the projet folder then you need to give path to the model "best.pt" which we trained.
