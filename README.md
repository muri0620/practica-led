# practica-led
  - Haz git clone de este repositorio
    ```bash
    git clone https://github.com/LuisC-web/practica-led.git
    ```
  - Hacer crear un rama con nombre "agregar-led" y cambia a esa rama
    ```bash 
    git branch agregar-led
    git checkout agregar-led
    ```
  -  Agregue en el main.py
    ```python 
      from machine import Pin
      import time

      led1 = Pin(15, Pin.OUT) 
      led2 = Pin(14, Pin.OUT) #Agrega esta linea

      while True:
          led1.on()
          led2.off() #Agrega esta linea
          time.sleep(1)
          led1.off()
          led2.on() #Agrega esta linea
          time.sleep(1)
    ```
  - Has un commit con los cambios sigue lo sisguientes comandos:
    ```bash
    git add .
    git commit -m "Agregando segundo led"
    ```
  - Cambia a la rama main y realiza el merge
    ```bash
    git checkout main
    git merge agregar-led
    ```
  - Ejecuta en Thonny 
       
