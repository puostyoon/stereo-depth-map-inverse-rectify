# stereo-depth-map-inverse-rectify
Source codes to rectify or unrectify depth map.

The disparity or depth estimation usually requires rectified image inputs, thus the output depth image is in rectified camera coordinate.
However, we usually need depth or disparity map of the original camera coordinate. That is, we need depth maps correspond to the unrectified (original) image.
![image](https://github.com/puostyoon/stereo-depth-map-inverse-rectify/assets/104057435/bfcc72f7-2beb-47f3-a020-21e83c5091d2)

Unrectifying depth images is not simply mapping xy pixel coordinates of the depth map, since the rectification process accompanies the change of camera position, thus the depth value must be changed.
This code unprojects a depth image into point cloud, apply transformation according to the new camera position, and projects the points into the depth map of the desired coordinate system.

Use example.ipynb.
