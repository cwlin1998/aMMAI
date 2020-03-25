# Deep Learning for Understanding Faces

Rajeev Ranjan, Swami Sankaranarayanan, Ankan Bansal,

Navaneeth Bodla, Jun-Cheng Chen, Vishal M. Patel,

Carlos D. Castillo, and Rama Chellappa



## Introduction

This paper introduces some deep learning methods in automatic face recognition.

There are mainly three modules in face recognition:

1. Face detection ( locate faces )
2. Key point detection ( locate important face key points )
3. Feature description ( extracting sufficient identifiable information )



## Methods

### Face Detection

- Region based
  - generates a pool of generic object-proposals, and use a DCNN to classify whether or not a given proposal contains a face
  - **drawback**: difficult faces are hard to capture in any object proposal
- Sliding-window based
  - computes a face detection score and bounding-box coordinates at every location in a feature map at a given scale
  - detections at different scales are typically carried out by creating an image pyramid at multiple scale
  - e.g. DP2MFD, DDFD

![](https://raw.githubusercontent.com/cwlin1998/aMMAI/master/paper%20reviews/w2/img/face_detector.png)

- Single-shot detector
  - a sliding-window-based detector
  - utilizes the inbuilt pyramid structure present in DCNNs reather than the pyramid mentioned above

### Key point detection

- Model based
  - learn a shape model during training and use it to fit new faces during testing
- Cascaded regression based
  - performance of regression-based approaches depends on the robustness of local descriptors
  - cascade of carefully designed DCNNs...

### Face identification and verification

- Robust feature learning for faces using deep learning

  - DeepFace, DeepID frameworks, FaceNet, VGGNet, etc.
  - Dataset: CASIA-WebFace, VGGFace

- Discrimitive metric learning for faces

  - Learn a classifier to improve the performance

- Implementation

  - subdivide into two tasks: face verification and face identification

- Training data sets for face recognition

  ![](https://raw.githubusercontent.com/cwlin1998/aMMAI/master/paper%20reviews/w2/img/dataset_face_recognition.png)

- Performance summary

  ![](https://raw.githubusercontent.com/cwlin1998/aMMAI/master/paper%20reviews/w2/img/performance_summary.png)

### Facial attributes

We are able to identify facial attributes such as gender, expression, age, skin tone, etc. Those attributes are very useful for apllications like image retrieval, emotion detection, and mobile security.

### MTL(MultiTask Learning) for facial analysis

**All-in-One Face** (Renjan et al.): a single DCNN model for simultaneous face detection, landmark localization, face recognition, 3-D head-pose estimation, smile detection, facial age estimation, and gender classification.

## Open Issues

#### Face detection

Due to the wide range of variations in the appearance of faces.

#### Fiducial detection

Most data sets contain only a few thou- sand images.

#### Face identification/verification

Due to memory constraints limited by graphics cards, how to choose informative pairs or triplets and train the network end to end using online methods on large-scale data sets is still an open problem.