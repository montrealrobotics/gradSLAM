# gradSLAM
Repo for the gradSLAM library (currently a stub)


### About gradSLAM

gradSLAM is a fully differentiable dense SLAM framework. It provides a repository of differentiable building blocks for a dense SLAM system, such as differentiable nonlinear least squares solvers, differentiable ICP (iterative closest point) techniques, differentiable raycasting modules, and differentiable mapping/fusion blocks. One can use these blocks to construct SLAM systems that allow gradients to flow all the way from the outputs of the system (map, trajectory) to the inputs (raw color/depth images, parameters, calibration, etc.).

Specifically, we implement differentiable versions three classical dense SLAM systems using the gradSLAM framework: KinectFusion, PointFusion, ICP-SLAM. We choose these because
* Each of these approaches sparked a new line-of-research in dense SLAM
* The approaches themselves are fairly simple from an algorithmic standpoint
* We aim to provide differentiable SLAM solutions for a wide variety of 3D representations (voxels, surfels, points).


### Expected release month

Thanks to the high quality reviews by the anonymous reviewers, we are working on improving gradSLAM and we expect to release the code in April 2020.
