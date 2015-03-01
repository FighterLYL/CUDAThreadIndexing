#CUDA Thread Indexing

This is intended as a quick reference about determining thread indexing in the CUDA C GPU Parallel Computing.

The repo will be updated frequently to include notes, information, and visual representation of the different forms of thread indexing related to different dimensions that occur in grids and blocks of a GPU. 

<img src="https://raw.githubusercontent.com/andreajeka/CUDAThreadIndexing/master/images/1dgrid1dblock.png" width="500px" height="312px" alt="1DGrid1DBlock"/>
```
int index = blockIdx.x * blockDim.x + threadIdx.x;
```



<img src="https://raw.githubusercontent.com/andreajeka/CUDAThreadIndexing/master/images/1dgrid2dblock.png" width="500px" height="313px" alt="1DGrid2DBlock"/>
```
// Specify the index for block scope before going to thread scope
int index = blockIdx.x * blockDim.x * blockDim.y + 
            threadIdx.y * blockDim.x + threadIdx.x;
```
