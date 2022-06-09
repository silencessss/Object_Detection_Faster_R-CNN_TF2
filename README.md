![TensorFlow](https://img.shields.io/badge/Tensorflow-%3E%3D2.4.1-orange)
![Python](https://img.shields.io/badge/Python-%3E%3D3.8-blue)

# Object_Detection_Faster_R-CNN_TF2
A TensorFlow 2.4.1 implementation of Faster R-CNN. This project is refer it.

## Requirements
- TensorFlow >=2.4.1
- Python >=3.8

## Implement detail(author)
- OS :Windows 10 with ANACONDA
- GPU :NVIDIA GeForce RTX 3060
- CPU :Intel(R) Core(TM) i5-9400F @ 2.90GHz
- Dataset :SnacksMIT

## Usage
### Train, Val
1. Weight. 
In the `frcnn.py`: line 25.
```
_defaults = {
        "model_path"    : 'model_data/voc_weights.h5',
        "classes_path"  : 'model_data/voc_classes.txt',
        "confidence"    : 0.5,
        "iou"           : 0.3
    }
```
2. Dataset.
- Format: VOC format.
- Run `voc2frcnn.py` to generate `.txt` file.
- Modified your `classes=[" "]`. In `voc_annotation.py`. Then, run it.
- Create a new `.txt` file which about classes. In the `model_data/new_classes.txt`.
- Modified the number of classes. In the `train.py`: line 121.

### Test (Inference)
1. Modified 2 parmas in `frcnn.py`: 'model_path' and 'classes_path'.
2. Modified 1 parmas in `predict.py`: line 27.
3. Run `predict.py`.

## Reference
- |github/bubbliiiing/faster-rcnn-tf2| [#link](https://github.com/bubbliiiing/faster-rcnn-tf2)
