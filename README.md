# Laboratorio de Redes - Tarea Programada (Cron Job)

#Lester Arana
#Usuario -> estudiante03


-VIDEO FUNCIONAMIENTO DE LA TAREA PROGRAMADA - https://drive.google.com/file/d/1_-OhVC0-uVyt-gVkJVdjeoIfUOP16gXu/view?usp=sharing

-PDF CON LA CREACION Y FUNCIONAMIENTO - https://drive.google.com/file/d/1XrKpmMPDMfIAMCLqbM9ISfr1JtNgBS1Q/view?usp=sharing



#Ejercicio a realizar
Crear una tarea programada (cron job) desde Webmin que ejecute el comando `ping` a `google.com` cada 15 minutos.



### 1. Ingreso a Webmin
- URL del laboratorio: [https://ct-redes.digicom.com.gt]
- Usuario: `estudiante03`
- Contraseña: `Seminario2025`

  -Imagen drive(https://drive.google.com/file/d/1XxeQIFB6pHmztVaiemcm8VaHzAyvao7M/view?usp=sharing)

### 2. Acceso a la sección de tareas programadas
Desde el panel lateral de Webmin accedí a:

-Sistema → Scheduled Cron Jobs

-Imagen drive ( https://drive.google.com/file/d/149FqIPPwijG8_VII5i8bWpvcqYr6Ayuu/view?usp=sharing )

### 3. Creación de la tarea programada

- Comando:
  bash
ping -c 4 google.com >> /root/ping_log.txt

- Frecuencia: cada 15 minutos (0, 15, 30, 45 en el campo “Minutes”)
- Horas, días, meses, días de la semana: All
- Estado: Activa (Yes)

-imagen drive(https://drive.google.com/file/d/1uriNUef3cTB48GK1Cq7VFUlVufVKSmJT/view?usp=sharing)


### 4. Verificación del funcionamiento
Después de esperar lapsos de 15 minutos desde la creación de la tarea, verifiqué el archivo de salida y obtuve la respuesta indicada.


PING google.com (142.250.217.206) 56(84) bytes of data.
64 bytes from mia07s61-in-f14.1e100.net (142.250.217.206): icmp_seq=1 ttl=117 time=29.4 ms
64 bytes from mia07s61-in-f14.1e100.net (142.250.217.206): icmp_seq=2 ttl=117 time=29.6 ms
64 bytes from mia07s61-in-f14.1e100.net (142.250.217.206): icmp_seq=3 ttl=117 time=28.6 ms
64 bytes from mia07s61-in-f14.1e100.net (142.250.217.206): icmp_seq=4 ttl=117 time=29.5 ms

-imagen drive(https://drive.google.com/file/d/1VKthrANIMjQp51w1zC3ucDi-PDp4iVxJ/view?usp=sharing)


### 5. Desactivación de la tarea
Para evitar que el servidor se sature 
- Fui al menu de la izquierda y luego a Scheduled Cron Jobs
- Seleccioné la tarea creada
- Presioné el botón Disable Selected
- 

### 6. Conclusión
Se logró crear y verificar una tarea programada funcional desde Webmin, automatizando el monitoreo de red (ping) cada 15 minutos y almacenando los resultados en un archivo. Posteriormente, la tarea fue desactivada para evitar sobrecarga innecesaria en el sistema.

## 7. Archivos generados
- /root/ping_log.txt → Archivo donde se almacenan los resultados del comando ping ejecutado cada 15 minutos.


  
