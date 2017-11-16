Управление коптером с Arudino
===

Для взаимодействия с ROS-топиками и сервисами на Raspberry Pi можно использовать библиотеку [rosserial_arduino](http://wiki.ros.org/rosserial_arduino).

Основной туториал: http://wiki.ros.org/rosserial_arduino/Tutorials

Arudino необходимо установить на Клевер и подключить по USB-порту.

Настройка Aruino IDE
---

Необходимо скачать и скопировать библиотеку ROS-сообщений Клевера в `<папка скетчей>/libraries`.

Настройка Raspberry Pi
---

Необходимо убедиться с в launch-файле Клевера (`~/catkin_ws/src/clever/clever/clever.launch`) включен запуск Arduino rosserial:

```xml
<arg name="arduino" default="true"/>
```

При изменении launch-файла необходимо перезапустить `clever_bundle`:

```bash
sudo systemctl restart clever
```