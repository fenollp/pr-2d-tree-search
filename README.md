# pr-2d-tree-search
Point-Region D-dimensional trees ([quadtrees](https://en.wikipedia.org/wiki/Quadtree#Point-region_(PR)_quadtree), [octrees](https://en.wikipedia.org/wiki/Octree), ...) [approximate nearest neighbor search](https://en.wikipedia.org/wiki/Nearest_neighbor_search) in near constant time.

Implementation of [2017: Almost constant-time 3D nearest-neighbor lookup using implicit octrees](https://link.springer.com/article/10.1007/s00138-017-0889-4).

The compactness & time complexity achieved in the mentioned paper may bring interesting results on CPU on octrees.

Then the idea is to adapt the approach to higher (and lower) dimensions and observe the possible time and space gains over costly L2-using approaches.

This is also a perfect project to personally investigate these areas in Rust:
* const generics
* benchmarking
* SIMD
* zero-copy techniques
* exposing a C++ ABI
* maybe GPU interaction

## TODO: Compare with other Rust octree impl:
* https://github.com/ybyygu/rust-octree
* https://github.com/dorsath/octree
* https://github.com/Nercury/octree-rs

## TODO: ANN over embeddings using L2 impl:
* https://github.com/facebookresearch/faiss (uses [2017: Billion-scale similarity search with GPUs](https://arxiv.org/abs/1702.08734))
* https://github.com/spotify/annoy
* https://github.com/microsoft/SPTAG
* maybe https://github.com/milvus-io/milvus
* maybe https://github.com/granne/granne
