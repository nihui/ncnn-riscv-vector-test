# ncnn-riscv-vector-test

This is ncnn scrfd face detection executable prebuild for riscv `rv64gc` / `rv64gcv` / `rv64gc_xtheadvector`

This is used to test single binary optimization for various riscv extensions.

The program will detect the CPU extensions at runtime and automatically select the best optimization path.

## usage

1. upload executable, model and image to your riscv board

```shell
scp scrfd scrfd_500m-opt2.param scrfd_500m-opt2.bin test.jpg root@192.168.1.70:/root/
```

2. run face detection

```shell
ssh root@192.168.1.70
chmod +x scrfd
./scrfd test.jpg
```

3. download output image and see the detection result

```shell
scp root@192.168.1.70:/root/image.png .
```

## tested

* milkv-duo-256m
* licheepi-4a
* canmv-k230
