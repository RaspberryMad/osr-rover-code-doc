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

Cada repositorio se puede descargar a cualquier dispositivo 

## 📑 Sobre este Repositorio

El propósito de **osr-rover-code-doc** es documentar cada archivo del repositorio `osr-rover-code`, manteniendo la misma estructura y actualizándose en sincronía con el código principal.

### 📌 Arquitectura del Proyecto

A continuación, se presenta un esquema de la arquitectura del proyecto para facilitar su comprensión:

## Archivos principales en la raíz
- `.gitignore` - Define archivos y carpetas a ignorar en el repositorio Git.
- `estructura.txt` - Documento que describe la estructura del proyecto.
- `LICENSE.txt` - Licencia del software del proyecto.
- `README.md` - Descripción general e instrucciones del proyecto.

## Directorios principales

### `config/`
Contiene archivos de configuración para la gestión de hardware y reglas del sistema:
- `60-i2c-tools.rules` - Configuración de reglas para herramientas I2C en Linux.
- `serial_udev_ubuntu.rules` - Reglas para asignación de puertos serie en Ubuntu.

### `init_scripts/`
Scripts para la inicialización del rover:
- `launch_osr.sh` - Inicia el software del rover.
- `osr_paths.sh` - Define rutas de entorno necesarias para OSR.
- `osr_startup.service` - Servicio systemd para iniciar OSR en el arranque.

### `ROS/`
Contiene los paquetes ROS para la integración del rover con ROS 2.

#### `ROS/led_screen/`
Manejo de la pantalla LED del rover.
- `CMakeLists.txt` - Configuración de compilación.
- `package.xml` - Metadatos del paquete.
- `src/arduino_comm.py` - Comunicación con Arduino.
- `src/screen.py` - Control y visualización de la pantalla.

#### `ROS/osr_bringup/`
Paquete de arranque del rover.
- `CMakeLists.txt` - Configuración de compilación.
- `package.xml` - Metadatos del paquete.
- `config/osr_params.yaml` - Parámetros generales del rover.
- `config/roboclaw_params.yaml` - Configuración del controlador de motores RoboClaw.
- `launch/osr_launch.py` - Script de lanzamiento de nodos ROS.

#### `ROS/osr_control/`
Control de hardware del rover.
- `package.xml` - Metadatos del paquete de control.
- `setup.py` - Script de instalación.
- `osr_control/rover.py` - Control general del rover.
- `osr_control/servo_control.py` - Control de servos.
- `osr_control/roboclaw.py` - Interfaz para RoboClaw.

#### `ROS/osr_gazebo/`
Simulación del rover en Gazebo.
- `package.xml` - Metadatos del paquete de simulación.
- `launch/empty_world.launch.py` - Inicia simulación en un mundo vacío.
- `launch/rviz.launch.py` - Configuración de RViz.
- `meshes/` - Modelos 3D del rover.
- `urdf/osr.urdf.xacro` - Modelo URDF del rover.

#### `ROS/osr_interfaces/`
Interfaces de comunicación ROS.
- `msg/CommandCorner.msg` - Mensaje ROS para el control de esquinas.
- `msg/CommandDrive.msg` - Mensaje ROS para el control de movimiento.
- `msg/Status.msg` - Estado del rover.

### `scripts/`
Scripts auxiliares para pruebas y configuración.
- `calibrate_servos.py` - Calibración de servos.
- `rc_config.py` - Configuración de radio control.
- `roboclawtest.py` - Prueba de motores con RoboClaw.
- `test_ina260.py` - Prueba del sensor de corriente INA260.

### `setup/`
Documentación y guías de configuración.
- `arduino.md` - Guía de configuración de Arduino.
- `rover_bringup.md` - Instrucciones de inicio del rover.
- `rpi.md` - Configuración de la Raspberry Pi.
- `serial_config_info.md` - Información sobre configuración serie.

#### `setup/images/`
Contiene imágenes de referencia.
- `detach_corner_assy.png` - Ensamblaje de la esquina del rover.
- `wheel_odom_example.png` - Ejemplo de odometría con ruedas.
