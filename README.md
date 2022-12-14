# Revopoint-Dual-Turntable
Research and documentation on the Revopoint Dual Axis Turntable

- Reseach -> [Photoalbum](https://photos.app.goo.gl/Gpw4DirpBiTtLEeU9)
- Revopoint Forum -> [Post](https://forum.revopoint3d.com/t/reverse-engineer-bluetooth-commands-for-dual-axis-turntable/17504/18)
- Revopoint FB -> [Post](https://www.facebook.com/groups/revopointgloballaunch/posts/)

Microprocessor details
- [FR801xH-SDK](https://gitee.com/freqchip/FR801xH-SDK)

Android Bluetooth Serial APP:
- (https://play.google.com/store/apps/details?id=de.kai_morich.serial_bluetooth_terminal)

Android Bluetooth Serial APP Macro template:
- (https://downgit.github.io/#/home?url=https://github.com/opensourcemanufacturing/Revopoint-Dual-Turntable/blob/main/revopoint_tt_serial_bluetooth_terminal_cfg.txt)

```
[CONFIRMED WORKING COMMANDS]

--------------------------------
The control template goes as follow:    +"command","action"="value";

It is important that the command;
- is written in all caps
- has no spaces
- starts with + and is terminated with ;

------------- TILT -------------
+CR,TILTVALUE=10;     (degrees - min -30 max 30)
+CR,TILTSPEED=10;     (max speed 6.62, larger values = lower speed)
+CR,TOZERO;           (tilts back to boot time zero)
+CR,STOP;             (stop any ongoing rotation operation)

+QR,TILTANGLE;        (query current tracked tilt value)      
+QR,TILTSPEED;        (query current set tilt speed value)

------------ ROTATE -------------
+CT,TURNANGLE=360;    (degrees - incremental, + or - values)
+CT,TURNSPEED=36;     (max speed 35.64, larger values = lower speed)
+CT,TOZERO;           (rotates back to boot time zero)
+CT,STOP;             (stop any ongoing rotation operation)

+QT,CHANGEANGLE;      (query current tracked rotation value)
+QT,TURNSPEED;        (query current set rotation speed value)

----------------------------------
```

```
[GATT CTRLL - DUMP HEX REFERENCE]
+CR,STOP;              2B 43 52 2C 53 54 4F 50 3B 
+CR,TILTSPEED=10.000   2B 43 52 2C 54 49 4C 54 53 50 45 45 44 3D 31 30 2E 30 30 30 
+CR,TILTVALUE=-20.00   2B 43 52 2C 54 49 4C 54 56 41 4C 55 45 3D 2D 32 30 2E 30 30 
+CR,TILTVALUE=0.0000   2B 43 52 2C 54 49 4C 54 56 41 4C 55 45 3D 30 2E 30 30 30 30 
+CR,TILTVALUE=20.000   2B 43 52 2C 54 49 4C 54 56 41 4C 55 45 3D 32 30 2E 30 30 30 
+CR,TOZERO;            2B 43 52 2C 54 4F 5A 45 52 4F 3B 
+CT,STOP;              2B 43 54 2C 53 54 4F 50 3B 
+CT,TOZERO;            2B 43 54 2C 54 4F 5A 45 52 4F 3B 
+CT,TURNANGLE=-360.0   2B 43 54 2C 54 55 52 4E 41 4E 47 4C 45 3D 2D 33 36 30 2E 30 
+CT,TURNSPEED=36.000   2B 43 54 2C 54 55 52 4E 53 50 45 45 44 3D 33 36 2E 30 30 30 
+QR,TILTSPEED;         2B 51 52 2C 54 49 4C 54 53 50 45 45 44 3B 
+QR,TILTVALUE;         2B 51 52 2C 54 49 4C 54 56 41 4C 55 45 3B 
+QT,CHANGEANGLE;       2B 51 54 2C 43 48 41 4E 47 45 41 4E 47 4C 45 3B 
+QT,TURNSPEED;         2B 51 54 2C 54 55 52 4E 53 50 45 45 44 3B 
00000;                 30 30 30 30 30 3B 
0000;                  30 30 30 30 3B 
000;                   30 30 30 3B 

https://github.com/opensourcemanufacturing/Revopoint-Dual-Turntable/blob/main/revoscan-turntable-serial-dump.txt
```
