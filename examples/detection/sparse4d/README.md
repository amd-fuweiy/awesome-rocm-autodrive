## Sparse4D
To enable training in AMD ROCm platform, small modifications are needed:

1. Prepare data
2. rename customer ops in projects/mmdet3d_plugin/ops to solve "ninja: error: build.ninja:26: multiple rules generate" issue:
````
cd projects/mmdet3d_plugin/ops
mv src/deformable_aggregation_cuda.cu src/deformable_aggregation_hip_cuda.cu
````
3. modify setup.py the cuda file name
4. Download pre-trained weights and Training
````
bash local_train.sh sparse4dv3_temporal_r50_1x8_bs6_256x704
````

We have also provided an [example](https://github.com/binding7012/Sparse4D) to provide out-of-the-box experience.
