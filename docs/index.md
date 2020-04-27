# 3D Scene Reconstruction from RGB-Depth Images

## Summary

We plan to build a 3D scene reconstruction system using data from an RGB-D camera. The 3D scene reconstruction system includes two major steps, visual odometry and point cloud meshing. From multiple frames of RGB-D images, we will first estimate the position and pose of the camera and build a dense point cloud representing objects in 3D. We will then construct 3D meshes from the generated point cloud. 

## Problem Description
3D scene reconstruction from multiple RGB-D images has recently become a popular research topic, as it can be applied in many emerging techniques, such as augmented virtual reality, gaming and robotics. Obtaining a reconstructed 3D model of a scene at high quality is thought to be a challenging task due to the difficulties in fusing noisy depth data into reliable 3D representation, artifact corrections, and building efficient and scalable algorithms to complete the task within a reasonable computing time. We plan to build a preliminary 3D scene reconstruction system that can reconstruct dense mesh of a room-scale environment. The system comprises two main parts: camera pose estimation and mesh reconstruction from point cloud. Camera pose estimation is important for merging point clouds observed in different frames to form a global point cloud for the complete scene. Mesh reconstruction from the point cloud will enable us to render realistic surfaces instead of points. 

We will solve the pose estimation problem using visual odometry with feature points. It uses non-linear optimization over camera poses and feature point positions to minimize the projection errors of feature points across different frames. This technique is called Bundle Adjustment. We will modify an existing stereo visual odometry system into an RGB-D visual odometry system. 

Mesh reconstruction of a 3D scene from a dense point cloud requires an efficient and robust algorithm to construct realistic scene objects from a large amount of noisy point data. We plan to implement the truncated signed distance function (TSDF), which represents the geometries as implicit functions by converting the point cloud into a volumetric form with each voxel storing the truncated signed distance from the camera. A mesh can then be extracted using the marching cube algorithm. To improve the memory efficiency of this approach, we plan to explore using adaptive data structures, octree and using hashing-based sparse voxel representation.  

## Goals and Deliverables

We plan to build a preliminary 3D Reconstruction system that can successfully reconstruct the mesh of a small-scale environment similar to the [BundleFusion project](https://graphics.stanford.edu/projects/bundlefusion/).
```markdown
Syntax highlighted code block

# Header 1
## Header 2
### Header 3

- Bulleted
- List

1. Numbered
2. List

**Bold** and _Italic_ and `Code` text

[Link](url) and ![Image](src)
```

For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/).

### Jekyll Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/Chengjie-Z/3D-scene-reconstruction/settings). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://help.github.com/categories/github-pages-basics/) or [contact support](https://github.com/contact) and we’ll help you sort it out.
