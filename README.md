# Integration-3.1

## 1. Create your PROJECT package and customize the package.xml

To create our packege we will follow the following tutorial: http://wiki.ros.org/ROS/Tutorials/CreatingPackage.

We will work with the catkin made in the previous lecture.

Inside the /src directory we create the "project_integration" package using the following command:

  $  catkin_create_pkg project_integration std_msgs rospy roscpp  
  
  Even if they are not need we have decided to create dependencies on std, rospy and roscpp.

This has created a Project directory which contains a package.xml and a CMakeLists.txt partially filled out.

We update the package.xml file with a description and we put ourselves as the mantainer. We also license it with the BSD licence. We don't change the dependencies.

## 2. Create a file with parameter year equals to 2018

As parameters are often written in yaml we will create a .yaml file named "year" with only the parameter year. Find it in the general directory.

## 3. Create a launch file that loads that parameter in the namespace /masteruvic

We create a launch directory and a file named file.launch.
In this file we write a rosparam load command that loads the year parameter.

If we launch the file (after cmake and sourcing the setup.bash in the devel folder) with the command

  $  roslaunch project_integration file.launch
  
and then we open another terminal and run

  $ rosparam get /masteruvic/year 
  
it prints "2018".

## 4. Add a rviz node to the launch file

We won't write the code we wrote as it can be found in the file "file.launch" inside the launch folder. It is the lines where we opena node by <node ...> and </node>.

When we launch the file now it opens a rviz window.

## 5.Include the file usb_cam-test.launch from the package usb_cam

The written code can also be find in the file.launch file. It is the part of the <include ...> </include>.

## 6. What are the arguments of usb_cam-test.launch?

The parameters found in the usb_cam node we find the parameters:

video device with argument /dev/video0, image_width with argument 640, image_height with argument 480, pixel_format with argument yuyv, camera_frame_id with argument usb_cam and io_method with argument mmap.

In the image_view node we only find the parameter autosize with argument true.


