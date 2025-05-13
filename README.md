# Reeborgs-World-Full-Maze

This project demonstrates a Python-based maze-solving algorithm in [Reeborg’s World](https://reeborg.ca/reeborg.html), where the robot (Reeborg) navigates through a complex maze using wall-following logic.

![Reeborg Maze Screenshot](https://github.com/user-attachments/assets/d8ab9149-a249-48af-837c-93f306eb014f)

## 🚀 What This Code Does

The robot follows the **right-hand rule** to solve the maze — a common strategy where Reeborg keeps its right side close to the wall. The logic ensures that it explores paths efficiently and eventually reaches the goal.

## 🔍 Logic Breakdown

- A custom `turn_right()` function is defined since Reeborg's World doesn't provide one by default.
- The main loop runs until `at_goal()` returns `True`, meaning the robot has reached the maze exit.
- Inside the loop:
  - If the front is clear and the right is also clear, the robot turns right and moves.
  - If only the front is clear, it just moves forward.
  - If there’s a wall in front, it checks whether it can turn right. If it can, it turns and moves. Otherwise, it turns left to continue exploring.

## 🧠 Concepts Practiced

- Looping and conditionals
- Custom function creation
- Logical operators (`and`, `not`)
- Algorithmic thinking for maze-solving

## 🧩 Code

~~~python
def turn_right():
    turn_left()
    turn_left()
    turn_left()
    
while not at_goal():
    while front_is_clear():
        if right_is_clear():
            turn_right()
            move()
        else: 
            move()            
    while wall_in_front() and not at_goal():
        if right_is_clear():
            turn_right()
            move()
        if wall_on_right():
            turn_left()
~~~

---

Feel free to fork this and try optimizing or using a left-hand wall-following rule instead!
