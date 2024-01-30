# jermaDetector
A Siamese Neural Network built to detect frames of Jerma in youtube videos.


This project was built before I better understood the TensorFlow API, so some of the methods I used to create the model may seem a bit odd.


Originally started as a joke when my friend hid a singular frame of Jerma, a popular Twitch streamer, in a 2.5 hour long Youtube video and said the first person to find it gets cookies.
In order to prepare for future competitions, I prepared this model. It was trained using augmented data of the LFW Dataset (seeing as it was built to detect a singular white man, I 
didn't see any issues using a dataset that mostly contains photos of white men), images I collected of Jerma, and lots of images I collected of anything that wasn't 
a face to make the model more robust in situations when a face wasn't present in the image. 


The final version of the model that I trained achieved an accuracy of 0.979. I suspect the model is biased against colored images, as only its negative training data contained colored images.

Youtube-DL is used to download the youtube video, with OpenCV being used to feed frames of the video into the model in batches. I optimized the model to process the video at 6x the normal
playback speed (the maximum that my friends had achieved while they were manually looking for Jerma was 5x the noraml playback speed). 
