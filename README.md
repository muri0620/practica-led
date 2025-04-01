Aquí tienes el código en **Markdown** correctamente formateado:  

# practica-led

## Pasos para agregar un segundo LED

### 1. Clonar este repositorio o hacer Fork
```bash
git clone https://github.com/LuisC-web/practica-led.git
```

### 2. Crear una nueva rama llamada "agregar-led" y cambiar a ella
```bash
git checkout -b agregar-led
```

### 3. Modificar el archivo `main.py` agregando el segundo LED
```python
from machine import Pin
import time

led1 = Pin(15, Pin.OUT)
led2 = Pin(14, Pin.OUT)  # Agrega esta línea

while True:
    led1.on()
    led2.off()  # Agrega esta línea
    time.sleep(1)
    led1.off()
    led2.on()  # Agrega esta línea
    time.sleep(1)
```

### 4. Guardar los cambios y hacer un commit
```bash
git add .
git commit -m "Agregando segundo LED"
```

### 5. Cambiar a la rama `main` y hacer el merge
```bash
git checkout main
git merge agregar-led
git push -u origin main
```

### 6. Ejecutar el código en Thonny
