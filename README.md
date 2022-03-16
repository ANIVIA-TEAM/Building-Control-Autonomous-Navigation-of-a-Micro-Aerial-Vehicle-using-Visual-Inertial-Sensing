# Building-Control-Autonomous-Navigation-of-a-Micro-Aerial-Vehicle-using-Visual-Inertial-Sensing

The purpose of this project is the production and software development of a small vertical take-off and landing platform which is equipped with a sensor package consisting of Inertial Measurement Unit (IMU), a downward facing camera and a single-beam height sensor and calculation devices and can perform online state estimation, control and autonomous navigation in a well-defined, controlled interior environment by using platform-mounted computer resources. This project which consists of computer-aided modeling, manufacturing, algorithm development, system integration and experimental phases, includes learning the theoretical materials necessary to implement control, navigation and state estimation algorithms. Mechanical parts such as platform body, landing gear and sensor mounting parts can be purchased or manufactured using 3D printers.However,electronics such as motors, electronic speed controllers, autopilot systems and computers will be purchased. The choice of the best combination of these parts will be made by the project team, taking into account the total flight time, aggressiveness level, maximum load capacity of the platform. The state estimation algorithm will work with the principle of fixing to the laboratory floor, detecting and simultaneously positioning and mapping (Simultaneous Localization and Mapping, SLAM) of a series of square labels called AprilTag. Due to the need for SLAM and autonomous navigation algorithms to run in real time, all calculations must be run on the platform and the C++ programming language must be used. The SLAM processing line can be summarized as follows: The camera which have enough square labels in the field of view collects images from the ground. It is the responsibility of the navigational algorithm to ensure that the platform does not fly outside the tag area and is not lost. An open-source AprilTag detection algorithm will detect the corners of the labels, recognize the tag IDs, and feed them to the following sequence of operations. These corners will then be used to predict the relative 6 degrees of freedom of the platform relative to each label, using computer vision techniques and especially multi-view projection geometry principles. The algorithm will also create a simultaneous tag map. The altitude measurement with the height sensor and the orientation estimation with the IMU will also be used with computer vision techniques to improve the accuracy of the pose estimation. The estimation will then be fed to a central Kalman filter, which is used to combine information from the IMU, height sensor and AprilTag detector to improve its accuracy. The robot will be ordered to move in a certain direction for a specific distance. The pose from the Kalman filter will be used to keep the platform in its time-parameter orbit. The robot is expected to follow certain basic orbits (suchas a spiral or diamond path). This project is separated from its counterparts with its ability to operate without GPS signals in a closed laboratory environment. With this new perspective, it has the potential to be a subject of a scientific article and to be presented at national/international conferences. In addition, it will provide an experimental mechanism for studies on Aerial Robotics.

APRILTAG

Apriltag library is used in this project mainly from https://github.com/AprilRobotics/apriltag

```https://github.com/AprilRobotics/apriltag.git```

An open source AprilTag library from is also used https://github.com/Tinker-Twins/AprilTag

Use this link to add Aptiltag library to your computer

```$ git clone https://github.com/Tinker-Twins/AprilTag.git```

USAGE

There is a algorithm inside this library which name is apriltag_opencv_demo

```cd build``` 

```cd bin```

Below code block runs apriltag_opencv_demo algoritm and takes images from media file of library. Then this algoritm detects apriltag 

```$ ./apriltag_opencv_demo ../../media/input/*.jpg```

RESULTS

Input file is created by project members and they are detected with apriltag algorithm. Output file is consist of detected apriltags. Input file consist of tag36h11 type aptiltags. Their photos are taken under some conditions. These conditions are light, photograph angles, apriltag surface, distance. With changing these parameters, detection capability of apriltag algoritm is observed.



