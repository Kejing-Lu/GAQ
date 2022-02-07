# Project Title

GAQ: Accelerating the Top-K Approximate Nearest Neighbor Search on Proximity Graphs via Graph-aware Quantization

## Getting Started

### Prerequisites

* OpenCV 3.30+
* GCC 4.9+ with OpenMP
* CMake 2.8+
* Boost 1.55+

### Datasets

* Gist: https://www.cse.cuhk.edu.hk/systems/hash/gqr/datasets.html
* ImageNet: http://www.cad.zju.edu.cn/home/dengcai/Data/ANNS/ANNSData.html
* Tiny: https://www.cse.cuhk.edu.hk/systems/hash/gqr/datasets.html
* Mnist: https://leon.bottou.org/projects/infimnist

### Query sets

* https://drive.google.com/file/d/1sVi8TxqBiql6o7NgwADv_pT1Uych6P9O/view?usp=sharing

### Ground truth sets

* https://drive.google.com/file/d/1umeZ1dXSgo0N3Fix7SwPXYqWyVNXqeS4/view?usp=sharing

### KNN graphs (for NSSG)
* https://drive.google.com/file/d/1xvZ0Swp3rFhU36RJiigV43tfmRLNmkzS/view?usp=sharing


### Compile On Ubuntu (Running on Gist)

* Put the dataset file, queryset file, ground-truth-set file(truth.gt) and KNN-graph file(for NSSG) into the same folder of the script(run_XXX.sh). 

Complie GAQ+HNSW

```shell
unzip GAQ+HNSW.zip
cd GAQ+HNSW
mkdir build
cd build
cmake ..
make
bash run_HNSW_gist
```

Complie GAQ+NSSG

```shell
unzip GAQ+NSSG.zip
cd GAQ+NSSG
cd SSG-master
mkdir build
cd build
cmake ..
make
bash run_NSSG_gist
```

## Parameters 

* `K` is the value of top-K.
* `n` is the size of dataset and `qn` is the size of query set.
* `d` is the dimensionality of the dataset.
