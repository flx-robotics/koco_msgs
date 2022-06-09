# KoCo Messages

This repository contains the messages, services, and actions used by the KoCo flexible control framework.

## Messages
* `DigitalIO`: Represents the state of a single digital input/output signal.
* `DigitalIOArray`: Represents the state of several digital input/output signals as an array of DigitalIO messages.
* `KocoPose`: A complete description of the robot state in terms of joints, flange pose, tool pose, and robot-specific configuration flags.
* `KocoTool`: Description of a robot tool in terms of name, transform, weight, and center of gravity.

## Services
* `PlanAndStore`: Service for obtaining a trajectory from a joint target with MoveIt.
* `SetOutputs`: Service for setting the output signals on the robot.
* `SetRobotSpeed`: Service for setting the robot speed.
* `TriggerString`: Service for triggers that require a string input.

## Actions
* `Move`: Used by the robot move action server.
* `MoveJ`: Used by the robot moveJ action server.
* `MoveL`: Used by the robot moveL action server.
* `MoveSequence`: Used for executing sequential moves previously added to a buffer.
