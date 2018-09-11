# ck-nntest-outputs
Reference outputs for `nntest`

`*-tensorflow-cpu` programs were used as reference source when possible or `*-armcl-opencl` otherwise.

Example command to run a program with validation:

```bash
ck run program:conv-tensorflow-cpu \
    --dataset_uoa=tensor-conv-mobilenets-v1-1.0-224 \
    --dataset_file=shape-1024-1-1-1-1001-1-0 \
```

**Note**: The same reference outputs are used for direct-convolution as for convolution programs. But all `directconv-*` programs fail to run when kernel size is other than 1, 3 or 5. It is not an error but a limitation of direct convolution.

**Note**: The same reference outputs are used for winograd-convolution as for convolution programs. But `winogradconv-armcl-opencl` program fails to run when kernel size is other than 3 or 5 or stride is not 1. It is not an error but a limitation of winograd convolution.