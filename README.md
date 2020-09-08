## What is Intel® Distribution of OpenVINO™ Toolkit ?

The OpenVINO™ Toolkit’s name comes from Open Visual Inferencing and Neural Network Optimization. It is largely focused around optimizing neural network inference, and is open source.

It is developed by Intel®, and helps support fast inference across Intel® CPUs, GPUs, FPGAs and Neural Compute Stick with a common API. OpenVINO™ can take models built with multiple different frameworks, like TensorFlow or Caffe, and use its Model Optimizer to optimize for inference. This optimized model can then be used with the Inference Engine, which helps speed inference on the related hardware. It also has a wide variety of Pre-Trained Models already put through Model Optimizer.

By optimizing for model speed and size, OpenVINO™ enables running at the edge. This does not mean an increase in inference accuracy - this needs to be done in training beforehand. The smaller, quicker models OpenVINO™ generates, along with the hardware optimizations it provides, are great for lower resource applications. For example, an IoT device does not have the benefit of multiple GPUs and unlimited memory space to run its apps.

## What are pre-trained models?

In general, pre-trained models refer to models where training has already occurred, and often have high, or even cutting-edge accuracy. Using pre-trained models avoids the need for large-scale data collection and long, costly training. Given knowledge of how to preprocess the inputs and handle the outputs of the network, you can plug these directly into your own app.

In OpenVINO™, Pre-Trained Models refer specifically to the Model Zoo, in which the Free Model Set contains pre-trained models already converted using the Model Optimizer. These models can be used directly with the Inference Engine.

## Downloading Intel® Distribution of OpenVINO™ Toolkit

Go to the [Intel official website](https://software.intel.com/content/www/us/en/develop/tools/openvino-toolkit.html), register and download the tool kit

## Choosing Models 

* Human Pose Estimation: [human-pose-estimation-0001](https://docs.openvinotoolkit.org/latest/_models_intel_human_pose_estimation_0001_description_human_pose_estimation_0001.html)

* Determining Car Type & Color: [vehicle-attributes-recognition-barrier-0039](https://docs.openvinotoolkit.org/latest/_models_intel_vehicle_attributes_recognition_barrier_0039_description_vehicle_attributes_recognition_barrier_0039.html)

* Text Detection: [text-detection-0004](https://docs.openvinotoolkit.org/latest/_models_intel_text_detection_0004_description_text_detection_0004.html)

## Downloading Models

To navigate to the directory containing the Model Downloader:
``
cd /opt/intel/openvino/deployment_tools/open_model_zoo/tools/downloader
``

* Downloading Car Metadata Model

``
sudo ./downloader.py --name vehicle-attributes-recognition-barrier-0039 --precisions INT8 
``

* Downloading Human Pose Model

``
sudo ./downloader.py --name human-pose-estimation-0001 
``

* Downloading Text Detection Model

``
sudo ./downloader.py --name text-detection-0004 --precisions FP16 
``
