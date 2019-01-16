# Integration-3.1

## 1. Create your PROJECT package and customize the package.xml

To create our packege we will follow the following tutorial: http://wiki.ros.org/ROS/Tutorials/CreatingPackage.

We will work with the catkin made in the previous lecture.

Inside the /src directory we create the Project package using the following command:

  $  catkin_create_pkg Project std_msgs rospy roscpp  
  
  Even if they are not need we have decided to create dependencies on std, rospy and roscpp.

This has created a Project directory which contains a package.xml and a CMakeLists.txt partially filled out.

We update the package.xml file with a description and we put ourselves as the mantainer. We also license it with the BSD licence. We don't change the dependencies.

## 2.Create a file with parameter year equals to 2018

As parameters are often written in yaml we will create a .yaml file named "year" with only the parameter year. Find it in the general directory.

## 3.Create a launch file that loads that parameter in the namespace /masteruvic

We create a launch directory and a file named ex3.launch.
In this file we write a rosparam load command that loads the year parameter.

## 4.
