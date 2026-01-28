# for_informatica
"""
# import turtle
#
# # Настройка окна и черепахи
# screen = turtle.Screen()
# screen.title("Рисуем машину")
# t = turtle.Turtle()
# t.speed(3)  # Скорость рисования (1-10, где 10 - самая быстрая)
# t.pensize(2)  # Толщина линии
#
# # Функция для рисования прямоугольника (для кузова и окон)
# def draw_rectangle(turtle, width, height):
#     for _ in range(2):
#         turtle.forward(width)
#         turtle.left(90)
#         turtle.forward(height)
#         turtle.left(90)
#
# # Функция для рисования круга (для колес)
# def draw_circle(turtle, radius):
#     turtle.circle(radius)
#
# # Рисуем нижнюю часть кузова машины
# t.penup()
# t.goto(-100, 0)  # Начальная точка для кузова
# t.pendown()
# t.fillcolor("blue")  # Цвет заливки кузова
# t.begin_fill()
# draw_rectangle(t, 200, 50)  # Основной кузов (длинный прямоугольник)
# t.end_fill()
#
# # Рисуем верхнюю часть кузова (кабину)
# t.penup()
# t.goto(-20, 50)  # Начальная точка для кабины
# t.pendown()
# t.fillcolor("blue")
# t.begin_fill()
# draw_rectangle(t, 80, 40)  # Кабина (меньший прямоугольник)
# t.end_fill()
#
# # Рисуем окна
# t.penup()
# t.goto(-10, 60)  # Первое окно
# t.pendown()
# t.fillcolor("lightblue")
# t.begin_fill()
# draw_rectangle(t, 30, 20)  # Переднее окно
# t.end_fill()
#
# t.penup()
# t.goto(30, 60)  # Второе окно
# t.pendown()
# t.fillcolor("lightblue")
# t.begin_fill()
# draw_rectangle(t, 30, 20)  # Заднее окно
# t.end_fill()
#
# # Рисуем колеса
# t.penup()
# t.goto(-70, -10)  # Первое колесо
# t.pendown()
# t.fillcolor("black")
# t.begin_fill()
# draw_circle(t, 20)  # Радиус колеса
# t.end_fill()
#
# t.penup()
# t.goto(70, -10)  # Второе колесо
# t.pendown()
# t.fillcolor("black")
# t.begin_fill()
# draw_circle(t, 20)
# t.end_fill()
#
# # Скрываем черепаху и завершаем
# t.hideturtle()
# screen.mainloop()  # Держим окно открытым
import turtle
from PIL import Image
import os
# Конвертация изображения в GIF, если оно в другом формате (например, PNG или JPG)
def convert_to_gif(input_path, output_path):
    img = Image.open(input_path)
    img.save(output_path, 'GIF')
# Если у вас изображение не в GIF, раскомментируйте и укажите пути
# convert_to_gif('background.png', 'background.gif')
# Настройка окна Turtle
screen = turtle.Screen()
screen.title("Turtle с фоновым изображением")
# Установка фона (укажите путь к GIF-файлу)
try:
    screen.bgpic("1_background.png")  # Устанавливаем изображение как фон
except turtle.TurtleGraphicsError:
    print("Ошибка: Убедитесь, что файл background.gif существует в той же папке, что и скрипт.")
    print("Также проверьте, что формат файла корректен (должен быть GIF).")
# Пример рисования поверх фона (например, простой круг)
t = turtle.Turtle()
t.speed(5)
t.penup()
t.goto(0, 0)
t.pendown()
t.fillcolor("red")
t.begin_fill()
t.circle(50)
t.end_fill()
# Скрываем черепаху и держим окно открытым
t.hideturtle()
screen.mainloop()
"""
