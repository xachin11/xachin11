import turtle
import random

# Set up the screen
turtle.bgcolor("black")
turtle.speed(0)  # Fastest drawing speed
turtle.pensize(2)

# Create a list of colors
colors = ["red", "orange", "yellow", "green", "blue", "purple"]

# Function to draw a spiral segment with a random color
def draw_spiral():
    color = random.choice(colors)
    turtle.color(color)
    for i in range(20):
        turtle.forward(i * 2)
        turtle.right(144)

# Draw multiple spirals with different angles and offsets
for i in range(12):
    turtle.right(30)
    draw_spiral()
    turtle.penup()
    turtle.forward(150)
    turtle.pendown()

turtle.hideturtle()  # Hide the turtle cursor
turtle.done()  # Keep the window open
