# tronxy-x5
Configure tronxy for ramps 1.4, Marlin

Spanish:

Buenas, 

En este repositorio iré dejando todas las mejoras que voy a añadir a la impresora Tronxy X5, una de ellas, fue el cambio de placa.
La placa original tiene un firmware no actualizable Marlin 1.1.5/6. No va mal, pero no es nada configurable, y no permite usar la placa con otros slicers como simplify3D o Cura.

Cambié por una placa staticboards OVM20 Lite.

La placa original tiene unos drivers A4988, con un consumo de 0.180A cada uno. Todos los drivers tienen el mismo voltaje/amperaje. 
Esto me sirve de referencia para calibrar los drivers de la nueva placa OVM20 Lite  con drivers DRV8825. En esta placa modifiqué los valores, poniendolos un poco mas altos. Eje X,Y = +0.200A y en el eje Z y Extruder = +0.300 [ACLARACION: esto significa que cuando medimos la corriente que consume la placa sin motores, en mi caso 0.150A, al conectarlo con repetier/proterface, y poner en funcionamiento el motor, deberé sumarle 0.200A/0.300A y subir o bajar el potenciometro hasta conseguir ese valor, en mi caso para el eje X,Y =0.150+0.200A; y Z,E=0.150+0.300A] 

El marlin ha sido cosa de probar velocidades y aceleraciones que desde mi primeros test hasta ahora ha habido muchos cambios.
