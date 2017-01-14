# Persistence Testbed: Labview Interface #


The Persistence Testbed will be used to develop advanced AUV health monitoring algorithms. It consists of a benchtop-mounted frame containing most of the Tethys AUV sensors and actuators, and a Labview interface to command the vehicle’s pitch-pack and to acquire, display, and log sensor data.

Figure 1 shows the layout:

* The pitch-pack consists of a large mass attached to a lead screw driven by a motor. The motor’s commanded position is sent by the main vehicle computer to the motor controller, and the motor’s actual position, current, and voltage are read by the main vehicle computer. The position of the mass is derived from the motor’s encoder. The main vehicle computer’s main control loop runs at 2.5Hz.

* Five external sensors will supplement the vehicle’s intrinsic sensors: an absolute mass position string potentiometer, a high-rate motor current sensor, a high-rate motor voltage sensor, and 2 vibration sensors. The external sensors will be read by a National Instrument DAQ.

* A Labview VI running on a Windows laptop will be used to control the pitch-pack and to acquire/display/log the data. A ZeroMQ server running on the same laptop but outside Labview will provide the bridge between Labview and the vehicle.

**Figure 1:**
![PL_fig1.png](https://bitbucket.org/repo/oG65MB/images/3999844056-PL_fig1.png)