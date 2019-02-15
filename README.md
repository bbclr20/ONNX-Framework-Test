
# ONNX-Franwork-Test

It's hard to migrate Deep Learning from research to production. For example, developers in the research team may use PyTorch but the result needs to be deployed on the smartphone with Tensorflow Lite. ONNX is a open format to represent deep learning models. With ONNX, developers can more easily to move models between different frameworks (e.g. PyTorch-> ONNX -> TensorFlow).

This repo has some examples to transfer the models between different frameworks.

## Environment

- Ubuntu: 16.04

- Python: 3.5

## Installation

- Tensorflow

- Caffe2

- PyTorch

- MXNet

- ONNX

## Tensorflow

Install onnx-tf package from pip.

    pip install onnx-tf

onnx-tf can be used in the Python script or CLI.

In python script:

    import onnx
    from onnx_tf.backend import prepare

    onnx_model = onnx.load("input_path")  # load onnx model
    output = prepare(onnx_model).run(input)  # run the loaded model

Use CLI:

From Tensorflow to ONNX: `onnx-tf convert -t onnx -i /path/to/input.pb -o /path/to/output.onnx`

From ONNX to Tensorflow: `onnx-tf convert -t tf -i /path/to/input.onnx -o /path/to/output.pb`

## Reference

[1] [https://github.com/onnx/onnx-tensorflow](https://github.com/onnx/onnx-tensorflows)
