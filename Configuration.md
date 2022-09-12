# Configuration

- Download the model SLOWFAST_32x2_R101_50_50 .pkl to the /home/slowfast/configs/AVA/c2 directory using the following link: https://dl.fbaipublicfiles.com/pyslowfast/model_zoo/ava/SLOWFAST_32x2_R101_50_50.pkl

- Open SLOWFAST_32x2_R101_50_50.yaml in the directory: /home/slowfast/demo/AVA and change the
content to the following:

  - line 8: add the path of the file you just downloaded in the previous step which is the pretrained model.
  
  - line 75: make sure that the path of the actions file(ava.json) in the directory slowfast/demo/ava is updated accordingly.
  
  - line 76: add the path of the input video that you want to run the inference on.

  - line 77: add the path of the output.


- open your conda environment and run the following commands:
  
  - cd SlowFast
  
  - python setup.py build develop

  - python tools/run_net.py --cfg demo/AVA/SLOWFAST_32x2_R101_50_50.yaml
