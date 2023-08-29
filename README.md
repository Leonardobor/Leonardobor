import turtle
import colorsys as cs

# Configuración inicial de la ventana
turtle.setup(800, 800)
turtle.speed(0)
turtle.tracer(10)
turtle.width(2)
turtle.bgcolor("black")

# Bucle para crear el patrón
for j in range(25):
    for i in range(15):
        # Calcula el color utilizando espacio de color HSV
        color = cs.hsv_to_rgb(i / 15, j / 25, 1)
        turtle.color(color)
        
        # Dibuja un cuarto de círculo
        turtle.right(90)
        turtle.circle(200 - j * 4, 90)
        turtle.left(90)
        turtle.circle(200 - j * 4, 90)
        
        # Dibuja un pequeño círculo en el centro
        turtle.right(180)
        turtle.circle(50, 24)

# Finaliza y oculta la tortuga
turtle.hideturtle()
turtle.done()
