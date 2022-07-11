# Gazebo

Para ejecutar [Gazebo](http://classic.gazebosim.org/) con ROS2, se necesita el paquete (gazebo_ros_pkgs)[https://index.ros.org/r/gazebo_ros_pkgs/github-ros-simulation-gazebo_ros_pkgs/#foxy].

Actualmente, el simulador [Gazebo](http://classic.gazebosim.org/) está implementado en localhost dentro del docker de PX4.

Esto se debe a que el simulador de Gazebo necesita lo siguiente para operar:

* Los modelos del dron, los cuales se generan de manera automática.

* Una instalación de ROS2 para correr el paquete (gazebo_ros_pkgs)[https://index.ros.org/r/gazebo_ros_pkgs/github-ros-simulation-gazebo_ros_pkgs/#foxy].

* Los scripts de ejecución de PX4 están automatizados para ejecución sobre localhost, y cambiarlo probó ser laborioso.

# Modelos por defecto

En la página de Gazebo, hay algunos tutoriales útiles, entre ellos puedo destacar:

* [Instalación de gazebo_ros_pkgs (ROS2)](http://classic.gazebosim.org/tutorials?tut=ros2_installing&cat=connect_ros).
* [Integración con cámara de profundidad](http://classic.gazebosim.org/tutorials?tut=ros_depth_camera&cat=connect_ros) (este modelo de cámara es el usado en el modelo de simulación del drone).

# Trabajo futuro

El objetivo es tener una imagen de Docker que implemente de forma separada el simulador del sistema de control. De forma de aislar todo lo relevante al simulador en sí, los modelos del dron y el mundo simulado.