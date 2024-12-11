# Setup
First setup python environment with pytorch 1.4.0 installed, **it's highly recommended to use docker image [pytorch/pytorch:1.4-cuda10.1-cudnn7-devel](https://hub.docker.com/layers/pytorch/pytorch/1.4-cuda10.1-cudnn7-devel/images/sha256-c612782acc39256aac0637d58d297644066c62f6f84f0b88cfdc335bb25d0d22), as the pretrained model and the code might be incompatible with higher version pytorch.**

then install dependencies for the experiment:

```
pip install -r requirements.txt
```

# Test

## Inference Using Pretrained Model on Raw Video
Download `FTCN+TT` model trained on FF++ from [here](https://github.com/yinglinzheng/FTCN/releases/download/weights/ftcn_tt.pth) and place it under `./checkpoints` folder
```bash
python test_on_raw_video.py examples/shining.mp4 output
```
the output will be a video under folder `output` named `shining.avi`
