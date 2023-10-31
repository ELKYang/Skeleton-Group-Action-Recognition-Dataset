# Skeleton Group Action Recognition Dataset

The Skeleton Group Action Recognition dataset is a specialized dataset we crafted based on the Volleyball dataset introduced by Ibrahim et al. in their 2016 paper[^1]. This dataset emphasizes the provision of skeletal data for group action recognition in volleyball, transformed from traditional visual data into structural skeletal sequences.

## Overview

- **Origin Dataset**: Volleyball dataset from the paper by Ibrahim et al.[^1].
- **Annotated Frames**: 4830 frames from 55 videos.
- **Group Activities**: Right set, Right spike, Right pass, Right winpoint, Left winpoint, Left pass, Left spike, Left set.
- **Primary Focus**: Extraction and understanding of skeletal sequences representing these group activities.

## Data Collection Process

1. **Frame Extraction**: Leveraging the bounding-box annotations of players from the work of Sendo and Ukita[^2], we extracted photographs of every athlete on the court.
2. **Skeletal Extraction**: Used `mmpose`[^3] for deriving skeletal structure from photos of individual players.
3. **Skeletal Sequencing**: After procuring individual skeletal sequences, we derived the group skeletal sequences for group action recognition.

## Dataset Structure

- **Training Videos**: 1 3 6 7 10 13 15 16 18 22 23 31 32 36 38 39 40 41 42 48 50 52 53 54
- **Validation Videos**: 0 2 8 12 17 19 24 26 27 28 30 33 46 49 51
- **Test Videos**: 4 5 9 11 14 20 21 25 29 34 35 37 43 44 45 47

Inside each video directory, annotated frames can be found as sub-directories (e.g., `volleyball/39/29885`). Each frame directory has 41 images.

## Conclusion

The Skeleton Group Action Recognition dataset offers insights into group dynamics in volleyball via skeletal structures. It's a step forward in sports analytics, biomechanics, and AI-driven sports training.

## References

[^1]: Mostafa S. Ibrahim, Srikanth Muralidharan, Zhiwei Deng, Arash Vahdat, Greg Mori. "A Hierarchical Deep Temporal Model for Group Activity Recognition." 2016 IEEE Conference on Computer Vision and Pattern Recognition (CVPR), 2016. [Dataset available here](https://github.com/mostafa-saad/deep-activity-rec#dataset).
[^2]: Kohei Sendo, Norimichi Ukita. "Heatmapping of People Involved in Group Activities." 16th International Conference on Machine Vision Applications (MVA), 2019.
[^3]: MMPose: A PyTorch Toolbox for Pose Estimation. Available at: https://github.com/open-mmlab/mmpose
