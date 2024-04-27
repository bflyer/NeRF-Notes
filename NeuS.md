# NeuS: Learning Neural Implicit Surface by Volume Rendering for Multi-view Reconstruction
## Purpose
Reconstructing objects and scenes with high fidelity from 2D image inputs.

## Previous Works
#### 1. DVR and IDR 
- Require foreground mask as supervision
- **Defect**: Easily get trapped in local minimum, and thus struggle with the reconstruction of objects with severe self-occlusion or thin structures.

#### 2. NeRF and its variants (neural methods)
- Use **volume rendering** to produce a neural scene representation with robustnesss of optimization, even for high ly complex objects.
- **Defect**: Extracting high-quality surfaces from this learned implicit representation is difficult because there are not sufficient surface constraints in the representation.

## Core Idea
#### 1. SDF
Represent a surface as the zero-level set of a signed distance function (SDF) and develop a new volume rendering method to train a neural SDF representation.

#### 2. New Volume Rendering Method
- Conventional volume rendering method causes inherent geomrtric errors (i.e. bias) for surface reconstruction.
- **Improvement**: Free of bias in the first order of approximation, thus leading to more accurate surface reconstruction even without the mask supervision.
