# V-REP-line-following-drone-master
CoppeliaSim (V-REP)


Understand code (non threaded script of Quadcopter_target )
1. local pathHandle = sim.getObjectHandle('Path')
‘Path’- name should be same as the name of the path you created . pathHandle is the variable name given to  ‘Path’
2.  sim.followPath(thisObjectHandle, pathHandle, changePositionOnly, 0, 0.17,15)
      Means:
          sim.followPath(number objectHandle,number pathHandle,
                          number positionAndOrOrientation,number relativeDistanceOnPath,number velocity,number accel)
        Parameters:
	objectHandle: handle of the object to be moved
pathHandle: handle of the path object
positionAndOrOrientation: a value between 1 and 3 (1: only position is modified, 2: only orientation is modified, 3: position and orientation is modified). Can be nil in which case 3 is applied.
relativeDistanceOnPath: a value between 0 and 1, where 0 is the beginning of the path, and 1 the end of the path. Make sure you selected the appropriate path length calculation method (refer to the path position calculation method section).
velocity: movement nominal velocity. 
accel: the acceleration/deceleration.
