# Backbone

Example of backbone model training is based on [pytorch vision](https://github.com/pytorch/vision), following the guide below to get better performance experience in ROCm!

## ResNet50
1. prepare code
````
cd resnet50
git clone https://github.com/pytorch/vision.git
````
2. MIOpen tuning (optional)
````
export MIOPEN_FIND_MODE=1
export MIOPEN_FIND_ENFORCE=4
bash run_train.sh
````
3. Train
````
unset MIOPEN_FIND_MODE=1
unset MIOPEN_FIND_ENFORCE=4
bash run_train.sh
````
4. Train with NHWC layout (optional)
````
export PYTORCH_MIOPEN_SUGGEST_NHWC=1
export PYTORCH_MIOPEN_SUGGEST_NHWC_BATCHNORM=1
````
also need to change layout of input and model:
````
data = data.to(memory_format=torch.channels_last) # in train.py line 28
model = model.to(memory_format=torch.channels_last) # in train.py line 248
model = torch.compile(model) # to get better performance
````
