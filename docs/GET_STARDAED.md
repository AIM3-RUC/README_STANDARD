# Demos

We also provide three demo scripts, implemented with high-level APIs and supporting functionality codes. Source codes are available [here](code_link).

## Demo1
This script performs inference on a single image.
```
python demo/demo_1.py arg1 arg2 ...
```

Examples:
```
python demo/demo_1.py --num_gpu 4 --batch_size 32 ...
```


# Prepare datasets
We support multiple public datasets including [COCO](data_link) etc.
Public datasets like [COCO](data_link) are available from official websites or mirrors.
Your folder structure should be as follows:

```
prjname
├── lib
├── tools
├── configs
├── data
│   ├── coco
│   │   ├── annotations
│   │   ├── train2017
│   │   ├── val2017
│   │   ├── test2017
│   ├── cityscapes
│   │   ├── annotations
│   │   ├── leftImg8bit
│   │   │   ├── train
│   │   │   ├── val
│   │   ├── gtFine
│   │   │   ├── train
│   │   │   ├── val
│   ├── VOCdevkit
│   │   ├── VOC2007
│   │   ├── VOC2012
```

# Test existing models on standard datasets
We provide testing scripts for evaluating an existing model on the whole dataset (COCO, etc.). The following testing environments are supported:

* single GPU
* multiple GPUs

Choose the proper script to perform testing depending on the testing environment.
```
e.g.
# single-gpu testing
python tools/test.py \
    ${CONFIG_FILE} \
    ${CHECKPOINT_FILE} \
    [--out ${RESULT_FILE}] \
    [--eval ${EVAL_METRICS}] \
    [--show]

# multi-gpu testing
bash tools/dist_test.sh \
    ${CONFIG_FILE} \
    ${CHECKPOINT_FILE} \
    ${GPU_NUM} \
    [--out ${RESULT_FILE}] \
    [--eval ${EVAL_METRICS}]
```

Optional arguments:

* num_gpus: how many GPUs you use
* dataset: the name of the dataset you use
* ...

Examples:
Assume that you have already downloaded the checkpoints to the directory `models/`.
```
e.g. 
python tools/test.py \
    configs/faster_rcnn/faster_rcnn_r50_fpn_1x_coco.py \
    checkpoints/faster_rcnn_r50_fpn_1x_coco_20200130-047c8118.pth \
    --show
```

# Training on stardard datasets
We also provide scripts for the training.
This section will show how to train predefined models (under [configs](config_link)) on standard datasets i.e. [COCO](data_link).

## Training on a single GPU
We provide `tools/train.py` to launch training jobs on a single GPU. The basic usage is as follows.

```
python tools/train.py ...
```

This tool accepts several optional arguments, including:

* `num_gpus`: details
* `datasets`: details

## Training on multiple GPU
```
python tools/train.py --multi_gpus ...
```
