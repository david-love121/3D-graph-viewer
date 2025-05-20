# Interactive 3D Function Viewer

This project is a web-based interactive 3D function viewer that allows users to input mathematical equations of the form `z = f(x,y)` and visualize them as 3D surfaces or point clouds. I built this together with Gemini to explore WebGL and create a handy tool for visualizing mathematical concepts. Generative AI was used to create this project and Gemini wrote the majority of the readme. 

## Features

*   **Equation Input:** Enter mathematical functions using `x` and `y` variables. Common math functions (e.g., `sin`, `cos`, `sqrt`, `pow`, `PI`, `E`) and operators (`+`, `-`, `*`, `/`, `**` for exponentiation) are supported.
*   **Rendering Modes:**
    *   **Surface Rendering:** View the function as a connected mesh.
    *   **Point Cloud:** View the function as a collection of individual points.
*   **Customizable Gradient:**
    *   Select a base color for the surface gradient.
    *   The gradient intensity is based on the Z-value of the surface.
*   **Lighting Options:**
    *   **Dynamic Lighting:** A directional light source provides shading and depth.
    *   **Flat Lighting:** A simpler lighting model based on surface orientation relative to the camera.
*   **Camera Controls:**
    *   **Mouse Orbit:** Click and drag on the main view to rotate the graph.
    *   **Mouse Zoom:** Use the mouse wheel to zoom in and out.
    *   **Keyboard Rotation:** Use `W`, `A`, `S`, `D` keys to rotate the graph vertically and horizontally.
    *   **Projection Toggle:** Switch between Orthographic and Perspective camera views.
*   **3D Rotation Gizmo:**
    *   A visual gizmo in the bottom-right corner indicates the X (red), Y (green), and Z (blue) axes.
    *   Click and drag on the gizmo axes to rotate the main graph.
*   **Bounding Box:** Toggle a wireframe bounding box around the graph's domain.
*   **Interactive Side Panel:** All toggles and customization options are available in a convenient side panel.

## How to Run

The application is served by a simple Go HTTP server.

1.  **Prerequisites:**
    *   Go (Golang) installed on your system.

2.  **Start the Server:**
    *   Navigate to the project's root directory (`/workspaces/go-dev-container/` in our setup).
    *   Run the Go server:
        ```bash
        go run main.go
        ```
    *   You should see a message: `Server started at http://localhost:8080`

3.  **Access in Browser:**
    *   Open your web browser and go to `http://localhost:8080`.
    *   The `index.html` file will be served, and you can start plotting!

## Controls Summary

*   **Main View:**
    *   **Left-Click + Drag:** Orbit camera around the graph.
    *   **Mouse Wheel:** Zoom in/out.
    *   **Keyboard `W`/`S`:** Rotate camera vertically.
    *   **Keyboard `A`/`D`:** Rotate camera horizontally.
*   **Gizmo (Bottom-Right):**
    *   **Left-Click + Drag on Axis:** Rotate graph around the selected world axis.
*   **Side Panel:**
    *   **Equation Input:** Enter your `z = f(x,y)` function.
    *   **Base Gradient Color:** Pick a color for the surface.
    *   **Toggles:**
        *   Show Bounding Box
        *   Enable Dynamic Lighting
        *   Use Perspective Camera
        *   Connect Dots (Surface)
    *   **Plot Button:** Renders the current equation.

## Technologies Used

*   HTML5
*   CSS3
*   JavaScript (ES6+)
*   WebGL (for 3D rendering)
*   Go (for the simple HTTP server)

---
*This README was put together by Gemini Code Assist, based on our collaborative work on this 3D Function Viewer.*