# MODEL ZOO

### Common settings and notes

- The experiments are run with pytorch 1.5.*, CUDA 10.*, and CUDNN 10.*.
- Training times are measured on our servers with 8 1080Ti GPUs (12 GB Memeory).
- Testing times are measured on our local machine with 1080Ti GPU. 
- The models can be downloaded directly from [Google drive](model_link) or [Baidu drive](model_link).

## Exp Task1 (e.g. Object Detection)

### Dataset1 (e.g. COCO)

| Model                    | GPUs |Train time(h)| Test time (ms) |   AP               |  Download | 
|--------------------------|------|-------------|----------------|--------------------|-----------|
|[ctdet\_coco\_hg](../experiments/ctdet_coco_hg.sh)       |   5  |109          | 71 / 129 / 674 | 40.3 / 42.2 / 45.1 | [model](https://drive.google.com/open?id=1cNyDmyorOduMRsgXoUnuyUiF6tZNFxaG) |
|[ctdet\_coco\_dla\_1x](../experiments/ctdet_coco_dla_1x.sh)  |   8  | 57          |  19 / 36 / 248 | 36.3 / 38.2 / 40.7 | [model](https://drive.google.com/open?id=1r89_KNXyDyvUp8NggduG9uKQTMU2DsK_) |
|[ctdet\_coco\_dla\_2x](../experiments/ctdet_coco_dla_2x.sh)  |   8  | 92          |  19 / 36 / 248 | 37.4 / 39.2 / 41.7 | [model](https://drive.google.com/open?id=1pl_-ael8wERdUREEnaIfqOV_VF2bEVRT) |
|[ctdet\_coco\_resdcn101](../experiments/ctdet_coco_resdcn101.sh)|   8  | 65          |  22 / 40 / 259 | 34.6 / 36.2 / 39.3 | [model](https://drive.google.com/open?id=1bTJCbAc1szA9lWU-fvVw52lqR3U2TTry) |
|[ctdet\_coco\_resdcn18](../experiments/ctdet_coco_resdcn18.sh) |   4  | 28          |  7 / 14 / 81   | 28.1 / 30.0 / 33.2 | [model](https://drive.google.com/open?id=1b-_sjq1Pe_dVxt5SeFmoadMfiPTPZqpz) |
|[exdet\_coco\_hg](../experiments/exdet_coco_hg.sh)       |   5  |215          | 134 / 246/1340 | 35.8 / 39.8 / 42.4 | [model](https://drive.google.com/open?id=1-5bT5ZF8bXriJ-wAvOjJFrBLvZV2-mlV) |
|[exdet\_coco\_dla](../experiments/exdet_coco_dla.sh)      |   8  |133          | 51 / 90 / 481  | 33.0 / 36.5 / 38.5 | [model](https://drive.google.com/open?id=1PFcEqN0KjFuq9XaqzB7TkVD3pvXZx04e) |

#### Notes

- you can add some experimental details here

### Dataset2

## Exp Task2
