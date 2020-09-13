This is a Face Recognition project written in Python.

The purpose of this program is to use create a model that is able to recognize the name of a certain person, given some pictures of the person itself that are used to train the model.

First there is the MCNN() face detector, which can find the faces inside a picture, and returns the rectangle containing them.
Then it uses a pretrained model, called FaceNet, to create the embeddings for each detected face.

The FaceNet output, with the corresponding labels, will be used to train a SVC model with a linear kernel that can then be used to make predictions on other pictures of which the subjects are unknown to the program. This time there can be more than one person inside the picture.

Finally the photos are plotted with a red rectangle containing the face and the relative predicted label.

Extra: if the probability related to the prediction is lower than a certain threshold, the predicted label will be '????'.

# Folder structure

## Required libraries and downloads
Download the program from this link:  (it may take a while) . After that unzip the FaceRec folder.
Once the process is over, open the FaceRec folder, find the executable with the face icon and cut it outside of the folder.

## Directories
On your desktop (or wherever you like) create the following folder structure:

* FaceRecognition_App
  * FaceRec --> contains the data you unzipped
  * people ---> contains multiple subdirectories, named after the person you want to train your model to recognize, and each of these must contain images of the related person (make sure there is only one face for each pictures, otherwise it might give an error...)
  * predictive_models --> this is where your models will be saved
   * to_predict ---> contains the images of which you want to detect and recognize the identity
      
The more images you will use to train the model, the better the predictions will be!

## Last steps
After having put some pictures, both in the 'people' and the 'to_predict' folder, click on the executable icon to run the app.

# How to use
First, you have to train a model on the people you want to recognize in other photos. Decide the name of the model you want to create in "new prediction model save name" and click on "TRAIN PREDICTION MODEL".

Then, select the path of the folder where you stored the images you want the program to scan and recognize faces and click on "PREDICT AND SHOW" (Remember to ticke the square on the right).
Or you can click on "REAL TIME PREDICTIONS" to activate you real-time webcam predictions with the selected model.

Enjoy!
