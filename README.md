## Installation

1.  First, be sure you have completed the [setup instructions for your Coral
    device](https://coral.ai/docs/setup/). If it's been a while, repeat to be sure
    you have the latest software.

    Importantly, you should have the latest TensorFlow Lite runtime installed
    (as per the [Python quickstart](
    https://www.tensorflow.org/lite/guide/python)).

2.  Clone this Git repo onto your computer:

    ```
    mkdir google-coral && cd google-coral

    git clone https://github.com/google-coral/examples-camera.git --depth 1
    ```

3.  Download the models:

    ```
    cd examples-camera

    sh download_models.sh
    ```

    These canned models will be downloaded and extracted to a new folder
    ```all_models```.

4. Install the OpenCV dependencies
    ```
    .\install_requirements.sh
    ``` 

## Running the Adjusted Bounding box model on the Coral Dev Board

1. Connect to the Dev Board by ```mdt```
2. Clone this repository on The Dev Board
3. Run the model on the Dev Board 
```
python3 detect.py --model ../all_models/mobilenet_ssd_v2_face_quant_postprocess_edgetpu.tflite
```