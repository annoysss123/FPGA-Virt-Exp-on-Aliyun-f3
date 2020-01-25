# FPGA-Virt-Exp-on-Aliyun-f3
For FCCM20 blind review

There are still some issues with the IP address on Aliyun F3 instances, currently we provide another server with Xilinx U200 FPGA for demonstrations.

# Environment
Ubuntu 16.04

Xilinx SDAccel 2018.3

# IP address
IP address: 101.6.64.180

# Login in
User name: fccm20

Passwd: fccm20

# Public Cloud Examples:
We provide public cloud examples using VGG-16 nework as input CNN model. There are 16 cores with the parallelism of 512 ops/cycle, and each four cores locate in a seperate DDR bank.

We give four examples: 1) four users, each with 25% resources; 2) three users with 50%:25%:25% resources; 3) two users with 75%:25% resources; 4) one user with 100% resources.

The throughput of each user will be printed.

To run the example with case 1:

```
./fccm20-demo-public-1-1-1-1.exe ./binary_container_1.xclbin
```

To run the example with case 2:

```
./fccm20-demo-public-2-1-1.exe ./binary_container_1.xclbin
```

To run the example with case 3:

```
./fccm20-demo-public-3-1.exe ./binary_container_1.xclbin
```

To run the example with case 4:

```
./fccm20-demo-public-4.exe ./binary_container_1.xclbin
```

# Private Cloud Examples
We provide two examples with VGG16 and Resnet50 as input CNN model, respectively. Both examples first use static compiler and dynamic compiler to generate the instruction files with two cores. Then, they use dynamic compiler to generate the instruction files with four cores.

The throughput of all cores and the compilation cost of the static and dynamic compiler will be printed.

To run the example with ResNet CNN model:

```
./fccm20-demo-private-resnet50.exe ./binary_container_1.xclbin
```

To run the example with VGG-16 CNN model:

```
./fccm20-demo-private-vgg16.exe ./binary_container_1.xclbin
```
