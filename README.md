# KoCo Messages

This repository contains the messages, services, and actions used by the KoCo flexible control framework.

## Basic messages [*msg*]
* _DigitalIO_: Represents the state of a single digital input/output signal.
* _DigitalIOArray_: Represents the state of several digital input/output signals as an array of DigitalIO messages.
* _KocoPose_: A complete description of the robot state in terms of joints, flange pose, tool pose, and robot-specific configuration flags.
* _KocoTool_: Description of a robot tool in terms of name, transform, weight, and center of gravity.

## Service messages [*srv*]
* _PlanAndStore_: Service for obtaining a trajectory from a joint target with MoveIt.
* _SetOutputs_: Service for setting the output signals on the robot.
* _SetRobotSpeed_: Service for setting the robot speed.
* _TriggerString_: Service for triggers that require a string input.

## Action server messages [*action*]
* _Move_: Used by the robot move action server.
* _MoveJ_: Used by the robot moveJ action server.
* _MoveL_: Used by the robot moveL action server.
* _MoveSequence_: Used for executing sequential moves previously added to a buffer.
