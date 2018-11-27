## Protocolo de transferencia sobre UDP

QUIC es un protocolo de transferencia implementado en el espacio de usuario sobre UDP. 
Si observas el tráfico de tu red de manera ocasional, verás que QUIC aparece como 
paquetes UDP.

Basado en UDP también usa números de puerto UDP para identificar servidores específicos
en una maquina dada.

## ¿Funcionará?

Hay empresas y otras configuraciones de red que bloquean el tráfico UDP en otros
puertos distintos al 53 (utilizado para DNS). Otros regulan esos datos de manera que hacen
que QUIC de un resultado peor que los protocolos basados ​​en TCP. No hay fin a lo que algunos
operadores pueden hacer.

En el futuro previsible, todo uso de transportes basados ​​en QUIC probablemente
tendrán que ser capaces de retroceder de manera elegante a otra alternativa (basada en TCP).
Los ingenieros de Google han mencionado previamente tasas de falla medidas con
porcentajes bajos de un solo dígito.

## ¿Mejorará?

Lo más probable es que si QUIC demuestra ser una valiosa adición al mundo de Internet
, la gente querrá usarlo y querrá que funcione en sus redes y entonces las empresas 
pueden comenzar a reconsiderar sus obstáculos. Durante los años en que el desarrollo 
de QUIC ha progresado, la tasa de éxito en todo Internet ha aumentado.
