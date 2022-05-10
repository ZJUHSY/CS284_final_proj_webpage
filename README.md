# CS284A Final Project: Pathtracer Speed-up Optimization Milestone

## Author

SONGYE HAN, University of California, Berkeley, USA\\
TIANYI HUANG, University of California, Berkeley, USA\\
MINGYUE FAN, University of California, Berkeley, USA\\
TIAN LIU, University of California, Berkeley, USA

## Proposal
[Proposal](https://drive.google.com/file/d/1vKKN-AYTG0D2O-WFNgM9-R2WFAyw4yAu/view?usp=sharing)

## Milestone Resource

### Milestone Report
[Report](https://drive.google.com/file/d/1Ys014uTI1Mt401NLYnRH_b0N2oIBlO3h/view?usp=sharing)

### Milestone Video
[Video](https://drive.google.com/file/d/1MwWJrM9GXvsf8VB7GlE9des_QDBKaoUy/view?usp=sharing)

### Presentation Slides
[Slides](https://docs.google.com/presentation/d/1nv6Ltf3IqgLssjAN94v8myT1iBDJW9hsFTqGJupNxpc/edit?usp=sharing)


## Final Deliverable

### Final Paper
[Report](https://drive.google.com/file/d/1T4s8yxhIZBzw9d04QIqChwFnEiuNdhfq/view?usp=sharing)

### Final Project Video
[Video](https://drive.google.com/file/d/1qIxpiXW8SOjzmzt8O9s1OF7ba-U0jqRX/view?usp=sharing)



<!-- ## 1 MILESTONE OVERVIEW
Until now We have made progress in optimizing both the memory and speed of our ray tracer based on the BVH accelerator. In addition, we also used kd-tree as an alternative accelerator to speed up the process. And we perform anti-aliasing optimization using the jittered sampling.

## 2 MEMORY OPTIMIZATION
The memory optimization process for BVH, could be addressed in the following 3 portions.
### 1. Memory Analysis of the original BVH buildup.
### 2. Optimization of Pointer Usage
### 3. Optimization of Coordinate system.
We’ve now successfully implemented the first 2 portions, with a mild setback on Memory Usage Analysis tool, and this is what we could be working on in the next part of the project. Our current progress for the 3rd part, is that it was easy to construct the new coordinate memory system, that for each double precision coordinate, we don’t need to note down the exact coordinate. Rather, we can note down the relative coordinate, relative to their parent. However, the difficulty was that it was hard to reconstruct the absolute coordinates after our memoization of relative coordinates, and a lazy algorithm, similar to segmentation tree, could be utilized.
## 3 SPEED UP
### 3.1 Morton Code based BVH Optimization
In this part, we will use Morton code based algorithm to optimize the efficiency of BVH.
After dividing the boxes according to the loaded data, we calculate the Morton code for each bounding box, and then sort it. In the sorted array, the order of each point is exactly the zigzag order in space. Although Morton code indicates the order of each point in the space, due to the zigzag sorting, there may be a gap between very few adjacent points. Although this will not affect the robustness of the overall algorithm, it may have a certain impact on the average
efficiency, because there might be a long bounding box in a certain dimension in the space.
For each interior, we compare its similarity with the two adjacent codes on the left and right. Here, we regard the BVH level bounding box corresponding to this interior as a fixed range in the array. After determining the direction of the range, you also need the size of the range to find the location of the two child nodes of the current interior within this range. The search principle we are based on is that within this range, the similarity of all Morton codes is similar to that of interior and other side codes.
We are currently working on building the above BVH structure. After we complete it, we can traverse the root of each bounding node from the bounding node to the corresponding bounding node. And in the searching process, we plan to create a stack. If it intersects with the bounding box of a node, we will press the corresponding node into the stack. And then cycle through each node in the stack until the it become empty.
### 3.2 KD-Tree
Instead of partitioning by objects using the BVH accelerator, we implement the KD-tree accelerator by partitioning the
space.
## 4 ANTI-ALIASING OPTIMIZATION
For Monte-Carlo integration Application, stratified sampling is always better than random sampling method. As random sampling for most of the time can not sample uniformly across the scene, the scenes rendered by random sampling have noise and aliasing under both low and high resolution. Stratified sampling(Jittered Sampling), in this case, can sample the light rays across the scene more uniformly by gridding up the unit square into cells and sampling light rays randomly in each cells of the grid. When implementing the stratified sampling, we need set up the number of samples equal to the square of an integer ahead of time in order to divide the square into cells for each sample later.
## 5 PROGRESS
### 5.1 Morton Code based BVH Optimization
Up to now, we have realized the Morton encoding of BVH nodes on the basis of understanding the principle, and we will complete the part of search through BVH in the next stage. And we currently do not see any improvements to build the accelerators. (Maybe we can set the maximum depth of the KD-Tree smaller), but we do not know the corresponding impact on the rendering process either. (We have not finished refactoring the rendering process until now).
### 5.2 KD-Tree Optimization
Until Now, after refactoring the code, we are able to construct the KD-tree accelerator. However, we have not refactored the rendering and visualization part to fit the KD-tree accelerator. (For the rendering part, the previous global illumination used the the BVH accelerator to calculate ray intersections). -->
