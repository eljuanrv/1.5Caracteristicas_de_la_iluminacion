# 1.5Caracteristicas_de_la_iluminacion
Es la quinta tarea del Primer Parcial de mi materia de Análisis y Procesamiento de Imágenes

## *INSTRUCCIONES*

Elegir una imagen sencilla en blanco y negro de internet, de preferencia un ícono de power point.
1. Imprimir la imagen a utilizar en una hoja blanca (el tamaño de la imagen abarque casi toda la hoja)
2. Usando python abrir la imagen virtual desde archivo y mostrarla en una ventana (la llamaremos imagen 1)
3. Usando python tomar una foto física desde webcam (o celular) y mostrarla en una ventana (la llamaremos imagen 2)
4. Observar las diferencias de iluminación y encuadre entre la imagen 1 y la imagen 2. Realizar ajustes en el ambiente en que se toma la imagen 2 y volver a tomarla (con python) intentando que las dos se parezcan lo mayor posible (la llamaremos imagen 3)
5. Escribir una conclusión con los ajustes que vieron necesarios para tomar la imagen 3

Entregar el trabajo en PDF, incluir en él:
- Código(s) utilizados
- Las tres imágenes tomadas
- 4 líneas (renglones) de conclusión en arial 12

```
import cv2
"""
En este caso, 0 quiere decir que queremos acceder
a la cámara 0. Si hay más cámaras, puedes ir probando
con 1, 2, 3...
"""
cap = cv2.VideoCapture(0)

leido, frame = cap.read()

if leido == True:
cv2.imwrite("foto.png", frame)
print("Foto tomada correctamente")
else:
print("Error al acceder a la cámara")

"""
Finalmente liberamos o soltamos la cámara
"""
cap.release()
```
