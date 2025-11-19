* Al descargar los archivos, dirígete a la ubicación de tu carpeta.
* Crea los dockers con "docker compose up -d --build".
* Ejecuta el servidor con "docker exec -it S1 bash".
* En la terminal del servidor. Inicia una captura en Wireshark con "tcpdump -i eth0 -w nombre_captura.pcap port 22". (Si no tienes tcpdump, debes instalarlo).
* En terminales separadas, ejecuta los contenedores para cada cliente. Luego, usa "ssh prueba@S1" para conectarte al servidor.
* Terminada la conexión, sal del servidor y usa "docker cp S1:/nombre_captura.pcap ." para que se genere la captura Wireshark y revisarla en dicho sniffer.
