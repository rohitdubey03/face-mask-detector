# FACE MASK DETECTOR

![alt text](https://github.com/rohitdubey03/face-mask-detector/blob/master/images/face_mask_detection_phases.png)

## Our current method of detecting whether a person is wearing a mask or not is a two-step process:

Step #1: Perform face detection

Step #2: Apply our face mask detector to each face

The problem with this approach is that a face mask, by definition, obscures part of the face. If enough of the face is obscured, the face cannot be detected, and therefore, the face mask detector will not be applied.

### We’ll be reviewing three Python scripts in this tutorial:

train_mask_detector.py: Accepts our input dataset and fine-tunes MobileNetV2 upon it to create our mask_detector.model. A training history plot.png containing accuracy/loss curves is also produced

detect_mask_image.py: Performs face mask detection in static images

detect_mask_video.py: Using your webcam, this script applies face mask detection to every frame in the stream


To circumvent that issue, you should train a two-class object detector that consists of a with_mask class and without_mask class.


Combining an object detector with a dedicated with_mask class will allow improvement of the model in two respects.


![alt text](https://github.com/rohitdubey03/face-mask-detector/blob/master/images/face_mask_detector_plot.png)

#### As you can see, we are obtaining ~99% accuracy on our test set.


