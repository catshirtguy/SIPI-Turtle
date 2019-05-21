# SIPI-Turtle

<p>The operating system (OS) used for the SIPI Turtle is <a href="https://www.ubuntu.com/download/desktop/thank-you?country=US&version=18.04.2&architecture=amd64">UBUNTU 18.04 LTS</a></p>

<p>Robot behaviors is programed using <a href="http://wiki.ros.org/kinetic/Installation/Ubuntu">ROS Melodic</a></p>

<p>Programming the power controller(Arduino Mega 2560) is done with the <a href="https://www.arduino.cc/en/Main/Software">Ardino IDE</a></p>

<h3>Software</h3>

<p>ROS USB cam Drivers</p>
<pre>sudo apt install ros-melodic-usb-cam</pre>

<p>  </p>
<pre>sudo apt install ros-melodic-image-transport</pre>

<p>ROS joystick drivers </p>
<pre>sudo apt install ros-melodic-joystick-drivers</pre>

<p> ? TBD </p>
<pre>sudo apt install ros-melodic-rosbridge-websocket</pre>



<h3>Debugging</h3>

<p>catkin build will not work if</p> <pre>ros-melodic-desktop</pre> <p> was installed. Catkin tools needs to be installed, use the following to install.</p>
<pre>sudo sh -c 'echo "deb http://packages.ros.org/ros/ubuntu `lsb_release -sc` main" > /etc/apt/sources.list.d/ros-latest.list'</pre>
<pre>wget http://packages.ros.org/ros.key -O - | sudo apt-key add -</pre>
<pre>sudo apt-get update</pre>
<pre>sudo apt-get install python-catkin-tools</pre>

<p>Image view may not work if ros full desktop was not installed. Use the following to install image view.</p>
<pre>sudo apt install ros-melodic-image-view</pre>



