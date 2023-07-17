## Importing OBJ Files Converted by a Plugin in Blender

The plugin #urdf_to_obj allows obtaining the mesh and precise positional information of a URDF file. Based on this, ensuring the accuracy of the robot model relies on controlling deformations.

After importing the OBJ file, for convenient further processing, the origin needs to be changed by selecting "Object Mode" and then using "Right Mouse Button" > "Origin to Center of Mass." With this, the preparation work is complete.

## Skeleton Drawing

In "Object Mode," press "Shift + A" to create a new skeleton. Switch Blender to "Edit Mode," select "Visibility," and enable the visibility of the skeleton while keeping it in the foreground. Click on the sphere above the skeleton to control its scale, and hold "Ctrl" for precise control. Then, press "E" to extrude the skeleton and correspond each active joint.

![Enable Visibility](https://guanboang.oss-cn-beijing.aliyuncs.com/img/Pasted%20image%2020230717165430.png)

During the process, the precision of the skeleton can be controlled using the origin's positional information.

![Origin Positional Information](https://guanboang.oss-cn-beijing.aliyuncs.com/img/Pasted%20image%2020230717170153.png)

At the bending points of the robotic arm, if disconnections are needed, they can be achieved by breaking the connected items in the "Bone Properties" - "Relations."

![](https://guanboang.oss-cn-beijing.aliyuncs.com/img/Pasted%20image%2020230717171649.png)

Then, position the skeleton approximately.

Since precise coordinates were obtained through the origin during the skeleton drawing process, the position at the end of the robotic arm is accurate.

## Skeleton Binding

After completing the skeleton drawing, switch to Pose Mode, select the corresponding component and skeleton, and use "Ctrl + P" - "Bone" to perform binding. Also, if there are multiple inactive parts, they can be bound by selecting them together and using "Ctrl + P" - "Object."

## Adding IK in Blender

The most convenient method for animation in Blender is to add IK and limit the axes, which allows simulating the movement of the robotic arm easily.

In "Pose Mode," click on the created "Pose" - "Inverse Kinematics" - "Add IK to Bone" - "To Empty." Now, the empty object can be used as a target to control the robotic arm.

![](https://guanboang.oss-cn-beijing.aliyuncs.com/img/Pasted%20image%2020230717174252.png)

To show the axes, open "Axes" in the real world.

Based on the actual axes, add axis locks to the robotic arm in "Bone Properties" - "Inverse Kinematics."

![](https://guanboang.oss-cn-beijing.aliyuncs.com/img/Pasted%20image%2020230717174501.png)

At this point, the overall task is completed.


-----


#  OLD  Readme - UR5 Robotic Arm: Blender and FBX Files with Skeleton and IK

This document provides a description of the Blender and FBX files for the UR5 Robotic Arm that include skeleton rigging and inverse kinematics (IK) functionalities. A total of four Blender files have been uploaded.

## File Breakdown

### 1. UR5.blend

This file serves as the base file for setting up the skeleton. It contains the UR5 model, but the skeleton is not bound to any parts, and no IK is implemented.

### 2. UR5New.blend

In this file, the skeleton has been bound to the parts of the UR5 model. However, no inverse kinematics is applied.

### 3. UR5-2.blend

This is one of the two versions that include both skeleton binding and IK. UR5-2.blend has a specific binding sequence and adjustments to facilitate IK.

### 4. UR5-3.blend

Similar to UR5-2, this file also contains the skeleton bound to the UR5 parts, with inverse kinematics. However, it differs in the binding sequence and adjustments compared to UR5-2.

## Special Thanks

A special thanks to Nathan for providing guidance throughout the process. Additionally, thanks to Mauro for his URDF to OBJ conversion script which has been invaluable.

## Upcoming Tutorial

Please note that a detailed tutorial covering the processes involved will be written and uploaded here once everything is organized and finalized.

Keep an eye on this space for the tutorial update.

Thank you for your interest and support!
