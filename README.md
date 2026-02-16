# Practica-1---Flor-de-vida

Práctica 1: Geometría Generativa con Python en Blender.

1. La base Matemática: Coordenadas Polares
Para posicionar cualquier objeto en un círculo (como los centros de los círculos periféricos
de nuestra figura), no usamos coordenadas X e Y de forma directa, sino coordenadas
polares (r, Ɵ).
Para que Blender entienda dónde colocar un objeto, debemos convertir esas coordenadas polares
a Cartesianas usando las funciones trigonométricas básicas:

x = r·cos(Ɵ)   
x = r·sin(Ɵ)

Donde r es el radio (la distancia desde el origen) y Ɵ es el ángulo en radianes. En Python,
como el círculo completo tiene 360°, usamos math.radians() para convertir los grados a
un formato que las funciones sin y cos entiendan.

2. Lógica de Construcción
La figura "Flor de la Vida" se basa en un concepto simple: Desplazamiento del Centro.     
 Círculo Base: Dibujamos un círculo con centro en $(0, 0, 0)$.     
 Círculos Periféricos: Los centros de los siguientes círculos deben estar ubicados
exactamente sobre el perímetro del primer círculo.     
 El Patrón: Si queremos que la figura sea simétrica y perfecta (como la imagen roja),
necesitamos distribuir los centros uniformemente. Dividimos los 360° de la circunferencia
entre el número de círculos que queremos (en este caso, 6 círculos, por lo que el paso es de
60°).     

4. Algoritmo de la Práctica (Paso a Paso)      
 Paso 1: Configuración del entorno. Importar la librería bpy para controlar Blender y
math para los cálculos. Limpiar la escena para no encimar objetos en cada ejecución.     
 Paso 2: Definición de variables. Establecer el radio del círculo y el angulo_actual
(iniciando en 0).     
 Paso 3: Trazado del origen. Crear la primitiva de círculo en el centro exacto de la
escena.     
 Paso 4: Identificación de la repetición. Aquí es donde el alumno nota que para el
segundo círculo debe sumar 60° al ángulo, calcular la nueva $x, y$, y volver a ejecutar el
comando de creación.

<img width="829" height="631" alt="Captura de pantalla 2026-02-13 113948" src="https://github.com/user-attachments/assets/bcf098ff-0a51-40eb-87fb-a4ab0fa40330" />


5.Resultado

<img width="570" height="411" alt="Captura de pantalla 2026-02-13 114010" src="https://github.com/user-attachments/assets/1b977f22-069c-443d-8a5a-04d181957f01" />
