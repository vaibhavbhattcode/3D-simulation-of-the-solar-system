3D Solar System Simulation
Overview
This project is a 3D simulation of the solar system developed as part of a frontend developer assignment. Built using Three.js (r128) for 3D rendering, GSAP for smooth UI animations, and plain JavaScript for interactivity, it features a mobile-responsive web page with a visually appealing, professional interface. The simulation includes the Sun at the center with eight planets (Mercury to Neptune) orbiting at adjustable speeds, realistic lighting, and a glassmorphism-styled control panel. All mandatory requirements and bonus features (pause/resume, background stars, hover labels, dark/light mode, and camera movement) are implemented, ensuring a robust and engaging user experience.
Features
Mandatory Features

3D Scene:
Sun at the center with a glowing effect using MeshBasicMaterial.
Eight planets (Mercury to Neptune) orbiting with realistic distances and sizes, rendered as SphereGeometry with MeshPhongMaterial for shiny surfaces.
Orbital paths visualized as circular lines.
Smooth animations using THREE.Clock and requestAnimationFrame for consistent frame rates.

Lighting:
Point light at the Sun’s position for realistic illumination.
Ambient light to ensure all planets are visible.

Speed Controls:
Control panel with sliders for each planet to adjust orbital speeds in real-time.
Immediate animation updates when sliders are moved, implemented with plain JavaScript.

Bonus Features

Pause/Resume: Button to toggle animation state with GSAP-powered scale animation for visual feedback.
Background Stars: 2000 randomly positioned stars created with Points for a realistic space environment.
Hover Labels: Planet names appear on hover using raycasting and canvas-based sprites, with GSAP for smooth opacity transitions.
Dark/Light Mode: Toggle between dark and light themes with GSAP-animated transitions, enhancing accessibility.
Camera Movement: Interactive camera controls via OrbitControls (pan, zoom, rotate) and click-to-zoom on planets with GSAP-animated camera positioning.

UI and Design

Glassmorphism Control Panel: Semi-transparent with blur effect, rounded corners, and shadows for a premium look.
Custom Sliders: Styled with colored indicators matching each planet, smooth hover effects, and Roboto font for modern typography.
Responsive Design: Control panel repositions to the bottom on mobile devices, ensuring usability across screen sizes.
Animations: GSAP animates the control panel slide-in, slider appearances, button interactions, and theme transitions for a polished experience.

Setup Instructions

Clone or Download:
Download and extract the project zip file (YourName.zip).

Run the Application:
Open index.html in a modern web browser (e.g., Chrome, Firefox, Edge).
No local server is required as all dependencies are loaded via CDN.

Dependencies:
Three.js (r128): https://unpkg.com/three@0.128.0/build/three.min.js
OrbitControls: https://unpkg.com/three@0.128.0/examples/js/controls/OrbitControls.js
GSAP (3.12.5): https://cdnjs.cloudflare.com/ajax/libs/gsap/3.12.5/gsap.min.js
Ensure an internet connection to load these CDN-hosted libraries.

Folder Structure:
index.html: Main file with HTML, CSS, and JavaScript.
README.md: This documentation file.
demo.mp4: (To be added) Video showcasing the project.

How to Use

View the Simulation: Open index.html to see the 3D solar system with planets orbiting the Sun, accompanied by a starry background.
Adjust Speeds: Use the sliders in the control panel to change each planet’s orbital speed in real-time.
Pause/Resume: Click the "Pause" button to stop animations and "Resume" to continue.
Interact with Planets:
Hover over a planet to display its name.
Click a planet to zoom the camera to it with a smooth GSAP animation.

Camera Controls: Drag to rotate, scroll to zoom, or use touch gestures on mobile devices (if OrbitControls loads successfully).
Toggle Theme: Click "Switch to Light Mode" or "Switch to Dark Mode" to change the UI theme.
Responsive Design: Resize the browser or test on a mobile device to verify adaptability.

Code Explanation

Scene Setup: Three.js creates a scene with a perspective camera and WebGL renderer, optimized with antialiasing.
Sun and Planets:
Sun: A large sphere with MeshBasicMaterial for a glowing effect.
Planets: SphereGeometry with MeshPhongMaterial, positioned at scaled distances, animated using angle increments based on speed and THREE.Clock delta time.

Orbits: Circular paths drawn with BufferGeometry and LineBasicMaterial.
Labels: Canvas-generated sprites with planet names, toggled via raycasting on hover.
Controls:
Sliders dynamically created for each planet, updating speeds in the animation loop.
GSAP animates UI elements for smooth transitions.

Camera Interaction: OrbitControls enables mouse/touch controls; click-to-zoom uses GSAP for camera movement.
Theme Toggle: CSS classes switch between dark/light modes, with GSAP for visual feedback.
Error Handling: Graceful degradation if OrbitControls fails to load, ensuring core functionality remains intact.

Demo Video (To Be Recorded)
The demo video (2-3 minutes) should include:

Simulation Overview: Show the 3D solar system with orbiting planets, stars, and orbital paths.
Speed Controls: Adjust sliders (e.g., for Mercury and Jupiter) to demonstrate real-time speed changes.
Bonus Features:
Click pause/resume to toggle animation.
Hover over planets to show labels.
Click a planet to zoom in.
Toggle dark/light mode.
Demonstrate camera rotation and zoom (if OrbitControls works).

Code Walkthrough: Open index.html in an editor and explain:
Planet creation (planets array, SphereGeometry).
Animation loop (requestAnimationFrame, THREE.Clock).
Slider integration with speed updates.
GSAP usage for UI animations.

Responsive Design: Resize the browser or show on a mobile device.

Submission Instructions

Create a zip file named YourName.zip containing:
index.html
README.md
demo.mp4 (record the demo video as described above)

Use the subject line: Frontend Assignment - Your Name
Submit via email or as instructed by the assignment guidelines.

Notes

Browser Compatibility: Tested on Chrome, Firefox, and Edge; requires WebGL support.
Performance: Optimized for quick loading and smooth animations, with fallback behavior if OrbitControls fails.
Troubleshooting: If camera controls don’t work, check the console for CDN errors and ensure an internet connection. Clear browser cache or try an incognito window.
Code Quality: Well-commented, modular, and maintainable, with clear variable names and structured logic.

Evaluation Criteria Addressed

Three.js Usage: Accurate creation of 3D objects, lighting, and animations.
Animations: Smooth and responsive planetary orbits with real-time speed updates.
User Input: Precise handling of slider inputs and interactive features.
Code Structure: Clean, commented, and organized for readability.
UI and Presentation: Professional glassmorphism design, responsive layout, and engaging animations.
