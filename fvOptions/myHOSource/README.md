## myHOsource code for manual RPS change

#### Summary:

myHOSource code behaviour is changed from the original HOSource in that RPS values for the disk revolutions can be changed manually. This was changed in order to do simplier simulations without the need of overset so that we can match the thrust of the propeller to the drag of the boat. 

An example of code is the following:


newdisk
{

    type            myHOSource;
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
    diskRPS            3.1052; // This number can be changed and updates continuously 
   
   
}
