# Revopoint-Dual-Turntable
Research and documentation on the Revopoint Dual Axis Turntable

- Reseach -> [Photoalbum](https://photos.app.goo.gl/Gpw4DirpBiTtLEeU9)
- Revopoint Forum -> [Post](https://forum.revopoint3d.com/t/reverse-engineer-bluetooth-commands-for-dual-axis-turntable/17504/18)
- Revopoint FB -> [Post](https://www.facebook.com/groups/revopointgloballaunch/posts/)

Microprocessor details
- [FR801xH-SDK](https://gitee.com/freqchip/FR801xH-SDK)


```
https://github.com/opensourcemanufacturing/Revopoint-Dual-Turntable/blob/main/revoscan-turntable-serial-dump.txt

[GATT CTRLL]
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
```
