# Spinning Donut & 3D ASCII Visualizer (in C)

This is a series of progressively more advanced C programs, going from simple ASCII shapes to a full spinning 3D donut rendered in your terminal — with lighting, perspective, and matrix transformations.

Each file builds on the previous one to explain key concepts in computer graphics, rendered purely with text output.

[Demo](https://www.ris8z.com/projects/rendering-3d-donut/)
---

## File Breakdown

### `01-circle.c`
 **Draws a basic 2D circle**  
Loops through a grid of characters and uses the equation of a circle to print `#` if the point is inside the radius. Introduces basic distance calculations in 2D space.

---

### `02-sphere.c`
 **Simulates a 3D sphere in ASCII**  
Extends the idea of a circle to 3D by adding depth and uses the distance formula in 3D. Points close to the sphere surface are drawn to give the illusion of volume.

---

### `03-2dPlane.c`
 **Prints a simple 2D plane**  
This is a basic flat grid used as a reference "ground". It’s foundational for layering objects in later files.

---

### `04-sphereOn2dPlane.c`
 **Combines the 3D sphere with a 2D plane**  
Simulates depth and layering — the sphere "rests" visually on top of the plane. This introduces the idea of **Z-ordering** in rendering.

---

### `05-donut1Spin.c`
**First version of the spinning donut**  
Creates a rotating torus (donut) using parametric equations. It loops over angles, calculates 3D positions, and prints them as characters to simulate motion.

---

### `06-donut2Spin.c`
**Smoother and optimized donut spin**  
Enhances performance and fluidity. Optimizes math, clears frames properly, and refines the update logic for better visual output.

---

### `07-prospective.c`
**Adds perspective projection**  
Applies formulas that make objects **appear smaller when further away**. This gives a 3D feeling to the render, simulating how our eyes perceive depth.

---

### `08-matrix.c`
**Matrix transformations (rotation, scale)**  
Implements transformation matrices to manipulate object coordinates more efficiently. This is the foundation of most 3D graphics engines.

---

### `09-lightEffect.c`
**Adds simple lighting with normals**  
Simulates how light hits the donut’s surface using the dot product between surface normals and a light direction vector. This enhances depth by showing **light intensity** on different faces.

---

##  Build & Run

To compile any file, use:

```bash
gcc 05-donut1Spin.c -o donut -lm
./donut
```
