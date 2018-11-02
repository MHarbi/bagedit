Catkin version of https://bitbucket.org/daniel_dube/bagedit, which are scripts to manage ROS bag files.

This is a small collection of scripts to manage ROS bag files. For now you can trim a bag ang merge two bages 

# Getting started
* Checkout the bagedit node to a local ROS Stack:
{{{
#!bash
hg clone https://daniel_dube@bitbucket.org/daniel_dube/bagedit
}}}

* Setup your ROS environment. On Ubuntu with a ordinary ROS Diamondback installation, the following commands will do it:
{{{
#!bash
source /opt/ros/diamondback/setup.bash
export ROS_PACKAGE_PATH=`pwd`:$ROS_PACKAGE_PATH
}}}

* Run the script:
{{{
#!bash
rosrun bagedit bagtrim.py --help
}}}

# bagedit 
{{{
#!bash
usage: bagtrim.py [-h] [-s start_time] [-e end_time] [-o output_file] [-a]
                  bagfile

Trims the beginning and the and of a bagfile.

positional arguments:
  bagfile         path to a bagfile

optional arguments:
  -h, --help      show this help message and exit
  -s start_time   start time in seconds
  -e end_time     end time in seconds
  -o output_file  name of the output file
  -a              use absolute timestamps
}}}
