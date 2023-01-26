# occupancy-grid-literature-study

![tesla_occupancy_grid](https://user-images.githubusercontent.com/19706987/214466612-58242b33-9c54-4c78-8714-8773603a2ca7.jpg)

### Semantic Scene Completion from a Single Depth Image

### Submanifold Sparse Convolutional Networks

### VaxNeRF: Revisiting the Classic for Voxel-Accelerated Neural Radiance Field

### Direct Voxel Grid Optimization: Super-fast Convergence for Radiance Fields Reconstruction

### UNDERSTANDING PURE CLIP GUIDANCE FOR VOXEL GRID NERF MODELS

Hybrid Representation NeRFs. In the original NeRF (Mildenhall et al., 2020), a coordinate-based
MLP continuously represents a 3D scene compared to traditional explicit representations such as
voxel grids. However, slow and memory-intensive computation is required to render even a single
image due to the number of forward passes required for sampled points along rays before plugging
into volumetric rendering. Other work (Liu et al., 2020; Yu et al., 2021; Garbin et al., 2021; Hedman
et al., 2021; Reiser et al., 2021) have utilized a hybrid implicit-explicit representation to speed up
rendering. However, such methods still use coordinates and Fourier embeddings to represent the
input. More recent work propose learning the input features stored directly in voxel grid structures.
Due to learning better input representations, the MLPs used in these models can be smaller, and
density values can be used to prune calculations for voxels on the grid. DVGO (Sun et al., 2022)
represents the scene as an explicit density grid and learns feature grid along with a view-dependent
MLP to model color. TensoRF (Chen et al., 2022) factorizes the voxel grids as vectors and matrices,
allowing for a smaller memory footprint. InstantNGP (Muller et al., 2022) utilizes multiresolution ¨
hierarchies of hash tables to represent the learned feature grids and another MLP to predict density
and color. Plenoxels (Fridovich-Keil et al., 2022) learns a sparse voxel grid of density values and
spherical harmonic coefficients for color. ReLU Fields (Karnewar et al., 2022) also utilizes explicit
density grids with spherical harmonics for color and shows that using ReLU activation after interpolating query point in the grid result in competitive results. Our work builds on DVGO. In the explicit
voxel grid model, the density and color grids are optimized directly with no neural networks. This is
akin to learning alpha and RGB values in an image directly in the 2D case. For the implicit version,
we use neural networks to predict the density and color grids.
