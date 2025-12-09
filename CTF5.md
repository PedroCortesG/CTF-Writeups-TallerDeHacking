#### Muchos dominios
Primero abri el pcapng con wireshark y busque "cc5325" y "{" pero el primero no me dio nada y el segundo muchos resultados. Por lo que luego use strings en la terminal con la forma vista en el auxiliar y consegui la flag.

#### Hora de exfiltrar
Abri el pcapng con wireshark, por enunciado supuse que no serviria buscar simplemente la flag pero igual lo intente, no me dio nada. Estuve viendo que podria tener algo que ver con la hora pero como no se me ocurrio nada, pague la pista. Con esta busque los ntp en wireshark, segui el stream y copie el texto de todos a un key.log (no se si eran necesario todos, probablemente habian repetidos entre diferentes consultas pero asi me asegure de tener todas las key). Con el key.log puesto en wireshark como se hace en el apunte, busque diferentes protocolos que pudieran servir hasta que llegue a http2. Vi algunas request hasta que encontre una que decia "get /flag ..." lo que supuse que era algo que ver con la flag. Vi el stream y busque en el url con el path que decia y encontre la flag.

