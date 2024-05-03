# Basic-Human-Activity-Recognition-Using-TIny-ML
Arduino Nano 33 BLE Sense can be used to recognize gestures using machine learning. A tensorflow model is designed, built and trained using accelerometer and gyroscope sensors data on Google Colaboratory, which can handle jupyter notebooks online. The model is converted to tensorflow-lite model and later encoded on Arduino Nano 33 BLE Sense header file. A a gesture classifier uses the model to classify the data from both sensor types. IMU has numerous sensors including accelerometer, gyroscope and magnetometer. In this project, we are going to use accelerometer and gyroscope data to predict punch and flex gesture.
# Collect accelerometer and gyroscope sensor data
To capture the accelerometer and gyroscope data, A sketch is written on arduino IDE and uploaded to the board. The sketch in this repository is labelled nano-33-gesture. Set up Arduino IDE. It helps both in uploading inference models to Arduino Nano 33 BLE Sense as well as download training data from it in .csv format. 
# Google colaboratory data upload
Open google Colaboratory platorm, Move to Files. Drag and drop your punch.csv and flex.csv files in the sample_data folder. The Google colaboratory provides a Jupyter notebook that allows us to run our TensorFlow training in a web browser.
# Train neural network, build and train a model
While on the Google colaboratory platform, go trough the notebook till the end. Convertion of the trained model into tensorflow lite model is done near the end. When the model.h file is created under Files, click on the model.h file to download to your pc.
# Encode the model in arduino header file
Open accelerometer and gyroscope clasifier sketch on this repository named as nano-classifier.ino.
Open the downloaded model.h file on your favourite editor and copy the content. Paste in your new model.h file you created alongside the classifier sketch and save. Upload the sketch and turn to Serial Monitor on on Tools to view result. The confidence of each gesture will be printed to the Serial Monitor showing (0 = low confidence, 1 = high confidence)

