# Happy-Day Android-App

HappyDay is the frontend to the HappyDay project. The app has been created because it allows to collect as much training data as possible for the neural networks. Every cool programmer is in possession of an Android smartphone and can download the app. Be it on the way or cosy at home in front of the TV: You get the mobile phone out, start the app and take some pictures.

<a href="https://play.google.com/store/apps/details?id=de.data_mining.hs_esslingen.happyday" rel="some text">![alt text](https://lh3.googleusercontent.com/fhR9eIkBWnbDZJQXRGRbRndG9b80ZwxzjL19DBqddH4AAZS-y3huZy7w10bk8WxB1JI=w200)</a>

## Dependency

- Android Smartphone with Camera
- Android Version >= 5.0 (Lollipop)
- Internet Connection

## Third Party Components

- [CameraFragment](https://github.com/florent37/CameraFragment)

## App Funktional

To make it quick and easy to take pictures with the app, the camera has been integrated into the app directly via the[CameraFragment](https://github.com/florent37/CameraFragment). Thus, the images do not have to be retrieved via Intent from standard camera apps.

The app works as shown in the figure.

![](pictures/app-functional-diagram.PNG)

When a photo has been taken, the face is recognized and cropped using vision tools from the Android SDK. This reduces unnecessary overhead because the background usually contains no information about the emotions.


## Functions
![](https://lh3.googleusercontent.com/gDnmRHb3ObyAh5bVVEDbrld--FO4TenCbZjtPYu7zN-ud4oV7hWInPLSj1yHueep7gQW=h310-rw)

### ![](app/src/main/res/mipmap-mdpi/ic_upload.png) Labeling

Now you can label the emotion on the photo and send it to the cloud to extend our trainings data by hitting the Cloud-Uplode button. The date is send over http to our Server.

### ![](app/src/main/res/mipmap-mdpi/ic_tf.png) Evaluation

To test the emotions classification, the image can also be sent to the server without labeling by clicking on the tensorflow button. Then the image is classified by the CNNs in the server and sends the result back to the app.
