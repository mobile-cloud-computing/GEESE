# GEESE: Edge Computing Enabled by UAVs
GEESE is a novel UAV based system that enables the dynamic deployment of an edge computing infrastructure through the cooperation of multiple UAVs carrying cloudlets.
 
 * We quantify the performance of UAVs to transport cloudlets to the edge.
 * We demonstrate that an edge computing infrastructure can be formed through the cooperation of multiple types of UAVs via collaborative processing.
 * We develop an edge delivery model that estimates the amount of UAVs and capabilities of cloudlets required to satisfy a workload from a crowd of users.

### Portable cloudlets: Feasibility analysis ###

* Computing capacity and energy consumption of cloudlets
We analyze the computational capacity to handle the task consists of detecting prime numbers within a list of available numbers.
Prime number detection [Android Web server](https://github.com/mobile-cloud-computing/GEESE/blob/main/AndServer_With_Battery_Log.zip/ "Android Web server") and the [Java client](https://github.com/mobile-cloud-computing/GEESE/blob/main/PrimeNumberJavaClient.zip/ "Java Client")

### GEESE design and development ###

GEESE delivers cloudlets on demand to any environment to provide edge computing services to end-applications. 
**Figure 1:** A large group of users looking for computation support on the move, a) Using cellular network to reach remote cloud resources, b) Using Wi-Fi/Bluetooth to access constrained edge server in proximity, c) Using the cloudlet support provided by UAVs in proximity.
![Figure 1:](https://github.com/mobile-cloud-computing/GEESE/blob/main/Geese1.PNG)

### Collaborative processing ###
We implemented a proof-of-concept prototype that follows a master/worker topology. A worker is an idle device, and the master is an initiator device that triggers the execution.\
Master Android App () \
Workers Android App () with the pre-trained model and the label file\


The master is in charge of initiating the task and divide it into jobs based on the number of available devices. The master then sends each job to the workers in a round-robin fashion. Jobs are independent of each other. Thus, the success of the application is measured by the rate of completed jobs. Each worker then processes the job and promptly returns the task to the master once the task is finished.
The prototype application is developed in Android version 5.0.1 and implements a Convolutional Neural Network (CNN) model to recognize objects within images.
We consider a set of 50 images in a resolution of 224x224, which are collected from the [ImageNet](http://image-net.org/ " ImageNet")
We rely on a deep learning implementation that uses [TensorFlow](https://www.tensorflow.org/lite/ "TensorFlow") with a pre-trained and quantized [mobilenet_v1_1.0_224](https://www.tensorflow.org/lite/guide/hosted_models/ "mobilenet_v1_1.0_224") model for recognizing objects in the images.



