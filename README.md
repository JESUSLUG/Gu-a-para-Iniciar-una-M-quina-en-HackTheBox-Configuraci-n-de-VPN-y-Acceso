# Guia-para-Iniciar-una-M-quina-en-HackTheBox-Configuraci-n-de-VPN-y-Acceso

Recuerda que tienes que inicar session en HTB Labs

Para iniciar una máquina en HackTheBox (HTB), necesitas seguir algunos pasos, incluyendo la configuración de una conexión VPN para poder acceder a las máquinas de la plataforma. Aquí tienes una guía detallada:

1. **Registro y Suscripción**:
   - Asegúrate de tener una cuenta en HackTheBox. Si no tienes una, regístrate en su sitio web.
   - Asegúrate de tener una suscripción activa o puntos suficientes para acceder a las máquinas.

2. **Descarga del archivo VPN**:
   - Inicia sesión en tu cuenta de HackTheBox.
   - Ve a la sección "CONNECT TO HTB" en el panel de usuario.
   - ![image](https://github.com/JESUSLUG/Gu-a-para-Iniciar-una-M-quina-en-HackTheBox-Configuraci-n-de-VPN-y-Acceso/assets/116361712/ce68c9b8-2597-4de9-aa95-fe902336e01c)
   - Selecciona Machines.
   - ![image](https://github.com/JESUSLUG/Gu-a-para-Iniciar-una-M-quina-en-HackTheBox-Configuraci-n-de-VPN-y-Acceso/assets/116361712/e219ed73-201f-443f-91c5-0f2cf6c9b1f0)
   - Selecciona el archivo de configuración de VPN apropiado para tu sistema operativo (Windows, macOS, Linux).
   - ![image](https://github.com/JESUSLUG/Gu-a-para-Iniciar-una-M-quina-en-HackTheBox-Configuraci-n-de-VPN-y-Acceso/assets/116361712/91bc1774-ce85-497d-9faf-20e37518035c)
   - Descárgala con la configuración que más te convenga.
   - ![image](https://github.com/JESUSLUG/Gu-a-para-Iniciar-una-M-quina-en-HackTheBox-Configuraci-n-de-VPN-y-Acceso/assets/116361712/5880323f-bd76-4a8b-afeb-f05d329686c9)



3. **Instalación y Configuración de OpenVPN**:
   - Si no tienes OpenVPN instalado, descárgalo e instálalo desde [OpenVPN](https://openvpn.net/community-downloads/).
   - En sistemas Linux, puedes instalarlo usando un administrador de paquetes. Por ejemplo, en Ubuntu puedes usar:
     ```sh
     sudo apt update
     sudo apt install openvpn
     ```

4. **Conexión a la VPN**:
   - Una vez que tengas OpenVPN instalado, abre una terminal (o símbolo del sistema en Windows).
   - Navega hasta el directorio donde descargaste el archivo de configuración de VPN.
   - Conéctate a la VPN usando el siguiente comando:
     ```sh
     sudo openvpn --config <nombre_del_archivo>.ovpn
     ```
     Reemplaza `<nombre_del_archivo>` con el nombre del archivo de configuración de VPN que descargaste.
     En nuestro caso se llama "lab_Moroko.ovpn".
     ![image](https://github.com/JESUSLUG/Gu-a-para-Iniciar-una-M-quina-en-HackTheBox-Configuraci-n-de-VPN-y-Acceso/assets/116361712/bd36b5c1-406d-434c-b7b6-da13bc662fd5)



5. **Verificación de la Conexión**:
   - Primero, en nuestra terminal, nos tendría que salir algo así:
   - ![image](https://github.com/JESUSLUG/Gu-a-para-Iniciar-una-M-quina-en-HackTheBox-Configuraci-n-de-VPN-y-Acceso/assets/116361712/dfa2b4b6-5787-461e-8012-3ceb05371d95)
   - Luego, dentro de HTB, en la sección donde descargamos la VPN, nos tendría que salir algo así:
   - ![image](https://github.com/JESUSLUG/Gu-a-para-Iniciar-una-M-quina-en-HackTheBox-Configuraci-n-de-VPN-y-Acceso/assets/116361712/3c071655-c4a0-47af-b24d-76ed5591da70)
   - Ahora, nos dirigimos a la sección de "Machines" para iniciar una máquina.
   - Una vez elegida, seleccionamos "Join Machine" para iniciarla.
   - ![image](https://github.com/JESUSLUG/Gu-a-para-Iniciar-una-M-quina-en-HackTheBox-Configuraci-n-de-VPN-y-Acceso/assets/116361712/f547da88-1a47-44b4-8e11-0977e97cf2c3)
   - Ahora, si inició correctamente, tendremos algo así:
   - ![image](https://github.com/JESUSLUG/Gu-a-para-Iniciar-una-M-quina-en-HackTheBox-Configuraci-n-de-VPN-y-Acceso/assets/116361712/2bf12996-9266-43bb-a57f-7b81bb5dfc64)
   - En este caso, debemos verificar la conexión con la máquina.
   - También puedes hacer un ping a la máquina para verificar la conexión.

6. **Hosts**:
   - Para garantizar la conexión a la máquina, hay que agregarla a nuestros hosts conocidos. Para ello, editamos el archivo `/etc/hosts` con el siguiente comando:
   - `sudo nano /etc/hosts`
   - ![image](https://github.com/JESUSLUG/Gu-a-para-Iniciar-una-M-quina-en-HackTheBox-Configuraci-n-de-VPN-y-Acceso/assets/116361712/7a4e8b36-ff21-4114-ae25-f4cd0a5a14bf)
   - Una vez dentro, procedemos a agregar nuestra IP junto con la URL.
   - ![image](https://github.com/JESUSLUG/Gu-a-para-Iniciar-una-M-quina-en-HackTheBox-Configuraci-n-de-VPN-y-Acceso/assets/116361712/b104f806-cd88-4e25-9707-e3c777b5ed5a)
   - Si todo salió bien, podremos acceder a la página del desafío, utilizando `http://tudesafio.htb`
   - ![image](https://github.com/JESUSLUG/Gu-a-para-Iniciar-una-M-quina-en-HackTheBox-Configuraci-n-de-VPN-y-Acceso/assets/116361712/8fcbc2ec-2fbf-4db1-85be-b8cbd19d9953)





Recuerda que cada máquina en HTB puede tener diferentes configuraciones y desafíos, por lo que deberás ajustar tus tácticas y herramientas según sea necesario. ¡Buena suerte y disfruta de la experiencia de aprendizaje en HackTheBox!
No olvides que si cierras la terminal en donde se esta ejecutando la VPN, se perdera la conexion a esta. 
No olvides que luego de terminar el desafio de tu maquina seleccionada, quitarla de tus hosts. 
