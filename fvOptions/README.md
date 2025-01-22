## New codes for actuator disk propulsion

#### Summary:

HOSource is the original code using KT and KQ to create the actuator disk

HOSource2 is a clone of the first one created so that propulsion with overset using 2 propellers is possible as with the original code it was not found possible to achieve. This code is just a placeholder as it works for now but its not the optimal solution. Although it has been tested and works.

myHOSource allows for manual change of RPS values for the actuator disk. This allows for many options regarding simulation.

An example of code is the following:

newdisk
{

    type            myHOSource; //HOSource
    refBody         "Hull.*";
    actBody         rotatingZone;
    rotationDir  right;
    KTCoeff (0.4353939 -0.3077697 -0.3498695 0.6332219 -0.581741 0.16453162);  //Corrected full scale
    KQCoeff (0.0532072 -0.0315018 -0.01677563 0.0379111 -0.05302225 0.0166337); 
    diskRadius    1.4; // radius of propeller
    diskHub        0.1428; // relative hub, which is equal to hub(unit: m)/diskRadius(unit: m)
    diskDir         (0.99482867 0 -0.10351333);
    diskOrigin     (0  0 -5.48172);
    diskThickness    0.4; // the thickness of the propeller
    bladeNumber             4; // number of blades
    diskRPS            3.1052; 
   
}
