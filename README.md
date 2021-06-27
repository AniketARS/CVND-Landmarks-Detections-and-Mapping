
# Simultaneous (Computer Vision Nanodegree Project)
  
In this project, you'll implement SLAM (Simultaneous Localization and Mapping) for a 2 dimensional world! You’ll combine what you know about robot sensor measurements and movement to create a map of an environment from only sensor and motion data gathered by a robot, over time. SLAM gives you a way to track the location of a robot in the world in real-time and identify the locations of landmarks such as buildings, trees, rocks, and other world features. This is an active area of research in the fields of robotics and autonomous systems.

Below is an example of a 2D robot world with landmarks (purple x's) and the robot (a red 'o') located and found using only sensor and motion data collected by that robot. This is just one example for a 50x50 grid world; in your work you will likely generate a variety of these maps.

<img src='./images/robot_world.png' width=50% height=50%/> 

---

## Demo

To see the working of this project please to [3. Landmark Detection and Tracking.ipynb](3.&#32;Landmark&#32;Detection&#32;and&#32;Tracking.ipynb).

---

## Working

- **Implementation of [Robot Class](/robot_class.py)**

    <img src='./images/robot_class.png' width=50% height=50%/>

    > Landmark locations [x,y]:  [[2, 4], [5, 7], [6, 3]]

- **Implementation of Constraints Matrix/Vector**
    1. *Initial Constraints*
        
        <img src='./images/initial_constraints.png' width=40% height=40%/> 

    2. *Calculation of Omega and XI*

        <img src='./images/omega_xi_constraints.png' width=80% height=80%/> 

- **Calculation of mu**

    <img src='./images/solution.png' width=80% height=80%/> 

---

## Results

```bash
  1. Expected Points.
```

**Estimated Pose(s):**
    `[50.000, 50.000]
    [37.858, 33.921]
    [25.905, 18.268]
    [13.524, 2.224]
    [27.912, 16.886]
    [42.250, 30.994]
    [55.992, 44.886]
    [70.749, 59.867]
    [85.371, 75.230]
    [73.831, 92.354]
    [53.406, 96.465]
    [34.370, 100.134]
    [48.346, 83.952]
    [60.494, 68.338]
    [73.648, 53.082]
    [86.733, 38.197]
    [79.983, 20.324]
    [72.515, 2.837]
    [54.993, 13.221]
    [37.164, 22.283]`


**Estimated Landmarks:**
    `[82.679, 13.435]
    [70.417, 74.203]
    [36.688, 61.431]
    [18.705, 66.136]
    [20.437, 16.983]`

```bash
  2. Points generated from SLAM.
```

**Estimated Poses:**
`[50.000, 50.000]
[37.973, 33.652]
[26.185, 18.155]
[13.745, 2.116]
[28.097, 16.783]
[42.384, 30.902]
[55.831, 44.497]
[70.857, 59.699]
[85.697, 75.543]
[74.011, 92.434]
[53.544, 96.454]
[34.525, 100.080]
[48.623, 83.953]
[60.197, 68.107]
[73.778, 52.935]
[87.132, 38.538]
[80.303, 20.508]
[72.798, 2.945]
[55.245, 13.255]
[37.416, 22.317]`


**Estimated Landmarks:**
`[82.956, 13.539]
[70.495, 74.141]
[36.740, 61.281]
[18.698, 66.060]
[20.635, 16.875]`
