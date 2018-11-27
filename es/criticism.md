# Crítica

## UDP nunca funcionará

Muchas empresas, operadores y organizaciones bloquean o limitan las tasas 
del tráfico UDP fuera del puerto 53 (utilizado para DNS), ya que recientemente
ha sido principalmente utilizado abusivamente para ataques. En particular, algunos 
de los protocolos UDP existentes e implementaciones populares de servidor han sido 
vulnerables a ataques de amplificación donde un atacante puede hacer una gran 
cantidad de tráfico saliente para apuntar a víctimas inocentes.

QUIC tiene incorporada mitigación contra ataques de amplificación al exigir que el
paquete inicial debe ser de al menos 1200 bytes y por restricción en el protocolo
eso dice que un servidor NO DEBE enviar más de tres veces eso en respuesta
sin recibir un paquete del cliente en respuesta.

## UDP es lento en los núcleos

Esto parece ser la verdad, al menos hoy en 2018. Por supuesto, no podemos decir
cómo se desarrollará esto y cuánto de esto es simplemente el resultado de que
el rendimiento de transferencia de UDP no haya estado en el enfoque de los 
desarrolladores por muchos años.

Para la mayoría de los clientes, esta "lentitud" probablemente nunca sea perceptible.

## QUIC utiliza demasiada CPU

Similar al comentario de "UDP es lento" anterior, esto se debe en parte a que
el uso de TCP y TLS en el mundo ha tenido más tiempo para madurar, mejorar 
y obtener asistencia de hardware.

Hay razones para esperar que esto mejore con el tiempo. La pregunta es 
cómo y cuánto este uso extra de la CPU perjudicará a los implementadores.

## Esto es solo Google

No, no lo es. Google trajo la especificación inicial al IETF después de haberlo
probado ,a gran escala en Internet, que implementar este estilo de protocolo sobre 
UDP en realidad funciona y se desempeña bien.

Desde entonces, personas de un gran número de empresas y organizaciones han 
trabajado en la organización neutral de proveedores IETF para fabricar un protocolo 
estándar de transporte a partir de eso. En ese trabajo, los empleados de Google 
por supuesto han estado participando, pero también los empleados de un gran número 
de otras empresas interesadas en ampliar el estado de los protocolos de transporte
en Internet, incluyendo Mozilla, Fastly, Cloudflare, Akamai, Microsoft,
Facebook y Apple.

## Esto es una mejora demasiado pequeña

Eso no es realmente una crítica sino una opinión. Tal vez lo sea, y tal vez sea
demasiado poca mejora muy cercana en el tiempo desde que se envió HTTP/2.

Es probable que HTTP/3 se desempeñe mucho mejor en redes llenas de pérdidas paquetes,
ofrece saludos más rápidos de forma que mejorará la latencia tanto percibida como
real. Pero ¿hay suficientes beneficios para motivar a las personas a implementar 
soporte de HTTP/3 en sus servidores y para sus servicios? ¡El tiempo y las medidas de
rendimiento futuro seguramente lo dirán!