# 🛰️ NASA Rover Project Documentation

## 🚀 Introducción

Bienvenido a la documentación del repositorio **osr-rover-code-doc**, donde se encuentra toda la información detallada sobre el código fuente del Rover.

El **NASA-Rover-Project** es un proyecto que implementa un sistema de backlog para gestionar las tareas de desarrollo, organizándolas en diferentes estados:

- 📋 **Tareas creadas**
- 🎯 **Tareas asignadas**
- ⚙️ **Tareas en proceso**
- ✅ **Tareas realizadas**

## 🔗 Repositorios Vinculados

Este proyecto está vinculado con tres repositorios clave:

1. **📂 ros2_tutorials_ws**
   - Contiene todas las pruebas realizadas a partir de los tutoriales de ROS2 Humble.
   
2. **📖 osr-rover-code-doc** *(Este repositorio)*
   - Aloja toda la documentación detallada del repositorio `osr-rover-code`.
   - Aquí encontrarás la descripción completa del proyecto.

3. **🛠️ osr-rover-code** *(Repositorio principal)*
   - Contiene el código fuente ejecutable en el Rover.
   
![Arquitectura del Proyecto](https://github.com/user-attachments/assets/75afa196-6562-4630-875d-a01407e4becf)

## 📑 Sobre este Repositorio

El propósito de **osr-rover-code-doc** es documentar cada archivo del repositorio `osr-rover-code`, manteniendo la misma estructura y actualizándose en sincronía con el código principal.

### 📌 Arquitectura del Proyecto

A continuación, se presenta un esquema de la arquitectura del proyecto para facilitar su comprensión:

 C:.
ª   .gitignore - Define archivos y carpetas a ignorar en el repositorio Git.
ª   estructura.txt - Documento que describe la estructura del proyecto.
ª   LICENSE.txt - Licencia del software del proyecto.
ª   README.md - Descripción general e instrucciones del proyecto.
ª   
+---config
ª       60-i2c-tools.rules - Configuración de reglas para herramientas I2C en Linux.
ª       serial_udev_ubuntu.rules - Reglas para asignación de puertos serie en Ubuntu.
ª       
+---init_scripts
ª       launch_osr.sh - Script para iniciar el software del rover.
ª       osr_paths.sh - Define rutas de entorno necesarias para OSR.
ª       osr_startup.service - Servicio systemd para iniciar OSR en el arranque.
ª       
+---ROS
ª   ª   README.md - Descripción del código ROS para el rover.
ª   ª   
ª   +---led_screen
ª   ª   ª   CMakeLists.txt - Configuración de compilación para el paquete led_screen.
ª   ª   ª   COLCON_IGNORE - Indica que este paquete debe ser ignorado en la compilación.
ª   ª   ª   package.xml - Metadatos del paquete ROS.
ª   ª   ª   
ª   ª   +---src
ª   ª           arduino_comm.py - Comunicación con Arduino para la pantalla LED.
ª   ª           screen.py - Control y visualización en la pantalla LED.
ª   ª           
ª   +---osr_bringup
ª   ª   ª   CMakeLists.txt - Configuración de compilación del paquete de arranque.
ª   ª   ª   package.xml - Metadatos del paquete ROS.
ª   ª   ª   
ª   ª   +---config
ª   ª   ª       osr_params.yaml - Parámetros generales del rover.
ª   ª   ª       roboclaw_params.yaml - Configuración del controlador de motores RoboClaw.
ª   ª   ª       
ª   ª   +---launch
ª   ª           .gitignore - Ignora archivos generados en esta carpeta.
ª   ª           osr_launch.py - Script de lanzamiento para iniciar nodos ROS.
ª   ª           
ª   +---osr_control
ª   ª   ª   dimensions_wheels_illustration.png - Ilustración de dimensiones de las ruedas.
ª   ª   ª   package.xml - Metadatos del paquete de control del rover.
ª   ª   ª   setup.cfg - Configuración de instalación del paquete Python.
ª   ª   ª   setup.py - Script de instalación del paquete Python.
ª   ª   ª   
ª   ª   +---osr_control
ª   ª   ª       ina_260_pub.py - Publicador de datos del sensor de corriente INA260.
ª   ª   ª       joy_extras.py - Funcionalidades extra para el control por joystick.
ª   ª   ª       roboclaw.py - Interfaz de control para el RoboClaw.
ª   ª   ª       roboclaw_wrapper.py - Envoltorio para facilitar el uso de RoboClaw.
ª   ª   ª       rover.py - Control general del rover.
ª   ª   ª       servo_control.py - Control de los servos del rover.
ª   ª   ª       __init__.py - Indica que es un paquete Python.
ª   ª   ª       
ª   ª   +---resource
ª   ª   ª       osr_control - Recursos adicionales para osr_control.
ª   ª   ª       
ª   ª   +---src
ª   ª   ª       test_controller.py - Script de prueba del controlador del rover.
ª   ª   ª       
ª   ª   +---test
ª   ª           test_copyright.py - Verifica cumplimiento de derechos de autor.
ª   ª           test_flake8.py - Prueba de estilo de código con Flake8.
ª   ª           test_pep257.py - Prueba de documentación con PEP257.
ª   ª           
ª   +---osr_gazebo
ª   ª   ª   CMakeLists.txt - Configuración de compilación para simulación en Gazebo.
ª   ª   ª   package.xml - Metadatos del paquete Gazebo.
ª   ª   ª   README.md - Explicación sobre el paquete de simulación.
ª   ª   ª   
ª   ª   +---config
ª   ª   ª       controller_velocity.yaml - Configuración de controladores de velocidad.
ª   ª   ª       
ª   ª   +---launch
ª   ª   ª       empty_world.launch.py - Inicia simulación en un mundo vacío.
ª   ª   ª       rviz.launch.py - Lanza RViz con configuración predefinida.
ª   ª   ª       
ª   ª   +---meshes
ª   ª   ª       arm.stl - Modelo 3D del brazo del rover.
ª   ª   ª       body.stl - Modelo 3D del chasis del rover.
ª   ª   ª       body_axis.stl - Modelo 3D del eje del chasis.
ª   ª   ª       box_link.stl - Modelo 3D de un enlace de la estructura.
ª   ª   ª       rockerbogie_front_1.stl - Modelo 3D del sistema Rocker-Bogie delantero.
ª   ª   ª       rockerbogie_middle_1.stl - Modelo 3D del Rocker-Bogie central.
ª   ª   ª       rocker_bogie_final.stl - Versión final del sistema Rocker-Bogie.
ª   ª   ª       rocker_bogie_link_front.stl - Enlace frontal del Rocker-Bogie.
ª   ª   ª       rocker_bogie_link_middle.stl - Enlace central del Rocker-Bogie.
ª   ª   ª       rocker_bogie_link_rear.stl - Enlace trasero del Rocker-Bogie.
ª   ª   ª       turn_L.stl - Modelo de giro a la izquierda.
ª   ª   ª       turn_left_test.stl - Prueba de giro a la izquierda.
ª   ª   ª       turn_R.stl - Modelo de giro a la derecha.
ª   ª   ª       turn_right_test.stl - Prueba de giro a la derecha.
ª   ª   ª       wheel.stl - Modelo 3D de la rueda del rover.
ª   ª   ª       wheel_link_left_2.stl - Enlace de la rueda izquierda.
ª   ª   ª       wheel_link_right_2.stl - Enlace de la rueda derecha.
ª   ª   ª       wheel_middle_left.stl - Modelo 3D de la rueda central izquierda.
ª   ª   ª       
ª   ª   +---rviz
ª   ª   ª       rviz_settings.rviz - Configuración de visualización en RViz.
ª   ª   ª       
ª   ª   +---src
ª   ª   ª       osr_controller.cpp - Código fuente del controlador del rover en ROS.
ª   ª   ª       
ª   ª   +---urdf
ª   ª           gazebo.urdf.xacro - Modelo URDF para simulación en Gazebo.
ª   ª           insert_transmission.urdf.xacro - Transmisión del rover en URDF.
ª   ª           osr.urdf.xacro - Modelo principal del rover en URDF.
ª   ª           
ª   +---osr_interfaces
ª       ª   CMakeLists.txt - Configuración de compilación de las interfaces.
ª       ª   package.xml - Metadatos del paquete de interfaces ROS.
ª       ª   
ª       +---msg
ª               CommandCorner.msg - Mensaje ROS para el control de esquinas.
ª               CommandDrive.msg - Mensaje ROS para el control de movimiento.
ª               Status.msg - Mensaje ROS con estado del rover.
ª               
+---scripts
ª       calibrate_servos.py - Script para calibrar servos.
ª       make_readme_pdf.sh - Genera un PDF del README.
ª       rc_config.py - Configuración de radio control.
ª       roboclawtest.py - Prueba de control de motores con RoboClaw.
ª       roboclaw_movemotor.py - Mueve motores con RoboClaw.
ª       rpi_estop_test.py - Prueba del botón de parada de emergencia.
ª       rpi_gpio_test.py - Prueba de pines GPIO en Raspberry Pi.
ª       test_ina260.py - Prueba del sensor de corriente INA260.
ª       
+---setup
    ª   arduino.md - Guía de configuración para Arduino.
    ª   rover_bringup.md - Instrucciones para iniciar el rover.
    ª   rpi.md - Configuración de la Raspberry Pi.
    ª   serial_config_info.md - Información sobre configuración serie.
    ª   
    +---images
            detach_corner_assy.png - Imagen del ensamblaje de la esquina.
            wheel_odom_example.png - Ejemplo de odometría con ruedas.
