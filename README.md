import turtle

def draw_flower():
    turtle.color("red")
    turtle.begin_fill()
    for _ in range(36):
        turtle.circle(50, 60)
        turtle.left(120)
        turtle.circle(50, 60)
        turtle.left(10)
    turtle.end_fill()

def draw_bunny():
    # Draw bunny body
    turtle.penup()
    turtle.goto(0, -50)
    turtle.pendown()
    turtle.color("white")
    turtle.begin_fill()
    turtle.circle(50)
    turtle.end_fill()

    # Draw bunny ears
    turtle.penup()
    turtle.goto(-20, 20)
    turtle.pendown()
    turtle.color("pink")
    turtle.begin_fill()
    turtle.goto(-30, 60)
    turtle.goto(-10, 20)
    turtle.end_fill()

    turtle.penup()
    turtle.goto(20, 20)
    turtle.pendown()
    turtle.begin_fill()
    turtle.goto(30, 60)
    turtle.goto(10, 20)
    turtle.end_fill()

    # Draw bunny face
    turtle.penup()
    turtle.goto(0, 0)
    turtle.pendown()
    turtle.color("black")
    turtle.circle(10)  # Nose

    # Draw eyes
    turtle.penup()
    turtle.goto(-15, 10)
    turtle.pendown()
    turtle.dot(5)

    turtle.penup()
    turtle.goto(15, 10)
    turtle.pendown()
    turtle.dot(5)

def write_message():
    turtle.penup()
    turtle.goto(-150, -150)
    turtle.pendown()
    turtle.color("black")
    turtle.write("Chúc bạn Tuyền 20/10 vui vẻ,", align="center", font=("Arial", 16, "normal"))
    turtle.penup()
    turtle.goto(-150, -170)
    turtle.pendown()
    turtle.write("sống thọ và đỗ NV 1!", align="center", font=("Arial", 16, "normal"))

def main():
    turtle.speed(1)
    draw_bunny()
    turtle.penup()
    turtle.goto(70, -30)
    turtle.pendown()
    draw_flower()
    write_message()
    turtle.hideturtle()
    turtle.done()

if __name__ == "__main__":
    main()
