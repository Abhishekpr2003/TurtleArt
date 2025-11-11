# 🌀 Colorful Spiral Pattern using Python Turtle

## 📖 Overview
This Python project generates a **vibrant spiral pattern** using the `turtle` graphics module and the `colorsys` library.  
The design dynamically changes colors in a circular motion, creating a mesmerizing **rainbow swirl effect** on a black background.

## ✨ Features
- Dynamic **color transitions** using HSV color model (`colorsys.hsv_to_rgb`)  
- **Nested circular loops** to form geometric spiral shapes  
- High-speed drawing (`speed(0)`) for instant rendering  
- Beautiful **rainbow gradients** on a black canvas  

## 🧠 How It Works
1. The `turtle` module creates a drawing cursor (the “turtle”) that moves around the screen.
2. The `colorsys` library converts HSV (Hue, Saturation, Value) color values to RGB for smooth color transitions.
3. Two nested `for` loops:
   - The **outer loop (`i`)** controls how many large spiral cycles are drawn.
   - The **inner loop (`j`)** draws circular arcs and shifts hues gradually to create a flowing gradient.
4. Circles are drawn using:
   ```python
   circle(radius, extent)
   ```
   where `extent=90` creates quarter arcs for a square-like spiral shape.
5. `h += 0.05` gradually changes the hue value, resulting in a rainbow effect.

## 🧩 Code
```python
from turtle import *
import colorsys

speed(0)
bgcolor("black")
h = 0.5

for i in range(30):
    for j in range(20):
        c = colorsys.hsv_to_rgb(h, 1, 1)
        color(c)
        h += 0.05
        rt(90)
        circle(150 - j * 6, 90)
        lt(90)
        circle(150 - j * 6, 90)
        rt(180)
    circle(60, 100)

done()
```

## 🛠 Requirements
- Python 3.x  
- No extra installations needed (both `turtle` and `colorsys` are part of the standard library)

## ▶️ How to Run
1. Save the code as `color_spiral.py`
2. Open a terminal or IDE
3. Run:
   ```bash
   python color_spiral.py
   ```
4. A new window will open displaying the colorful spiral pattern 🌈

## 🖼 Example Output
A vibrant spiral composed of rainbow-colored arcs radiating from the center.

## 💡 Customization Tips
- Change background color:
  ```python
  bgcolor("white")
  ```
- Adjust speed:
  ```python
  speed(10)  # slower drawing
  ```
- Modify hue change rate for smoother gradients:
  ```python
  h += 0.02
  ```

## 📚 Concepts Used
- **Turtle Graphics** — procedural drawing library in Python  
- **HSV to RGB conversion** — smooth color cycling  
- **Loops and Geometry** — nested iterations to form patterns  

## 🧑‍💻 Author
**Abhishek P R**  
*Creative Python graphics and visualization enthusiast.*

## Contact 
Email - abhishekpr811@gmail.com
linkedln - www.linkedin.com/in/abhishek-p-r-57081a228

