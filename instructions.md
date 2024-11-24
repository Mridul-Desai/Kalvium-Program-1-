![Kalvium Logo](https://s3.ap-south-1.amazonaws.com/kalvi-education.github.io/front-end-web-development/Kalvium-Logo.png)

# Drawing App

## Overview

This project involves implementing a Drawing App where users can interact with a canvas element using their mouse. Users can select stroke colors, adjust the line width, and draw by clicking and dragging the mouse on the canvas. The application includes functionalities for managing mouse events, color selection, and line width adjustments.

## Completed Functions

### Task 1: Implement the Color Picker

- **Description:** Users should be able to select a stroke color using a color picker input. The selected color will be applied to any lines drawn on the canvas.
- **Hint:** When the color input changes, update the drawing context's `strokeStyle` to reflect the new color chosen by the user.
- **Usage:** The stroke color should change as soon as the user selects a new color from the color picker.

### Task 2: Implement the Line Width Adjuster

- **Description:** Users should be able to adjust the line width using a range slider. The selected width should control the thickness of the lines drawn on the canvas.
- **Hint:** Set up an event listener on the range input to update the displayed value and the context's `lineWidth` based on the slider's current value.
- **Usage:** The line width should adjust in real-time as the user changes the value of the slider.

### Task 3: Implement the Drawing Functionality

- **Description:** Users should be able to draw on the canvas by clicking and holding the mouse button. The app should track the mouse movement to draw continuous lines. Drawing should stop when the user releases the mouse button or moves the mouse outside the canvas.
- **Hint:** Manage the mouse's state (whether it is pressed or not) and keep track of the current and previous mouse positions to draw lines between them. Use event listeners to handle `mousedown`, `mousemove`, and `mouseup` events.
- **Usage:** The app should start drawing when the user clicks and holds the mouse button and stop drawing when the mouse button is released or the cursor leaves the canvas area.

## Usage

1. **Select Stroke Color:**
   - Use the color picker to choose a color for your drawing.
   
2. **Adjust Line Width:**
   - Use the range slider to adjust the thickness of the lines.

3. **Start Drawing:**
   - Click and hold the mouse button on the canvas to start drawing.
   - Move the mouse to create lines.
   - Release the mouse button to stop drawing.

## Test Cases

1. **Color Picker Functionality:**
   - Should update the stroke color when the color picker value changes.
   - Test by selecting a color and verifying that the canvas uses the new color for drawing.

2. **Line Width Adjuster Functionality:**
   - Should update the line width when the range input value changes.
   - Test by adjusting the range slider and checking if the line width on the canvas changes accordingly.

3. **Drawing Functionality:**
   - Should allow drawing when the mouse is pressed down, and should stop when the mouse is released or leaves the canvas.
   - Test by drawing on the canvas and verifying that the drawing starts and stops as expected.

---

The HTML and CSS code are already provided. You need to implement the functionality in `app.js`. 

---
**Key Hints for Working with Canvas:**
**Canvas Basics**
- The <canvas> element in HTML is a drawing surface. Think of it as a blank sheet of paper you can draw on using JavaScript.
- To draw, you need to use the getContext("2d") method, which gives you a context object with methods for drawing shapes, paths, and more.
- ```const context = paintCanvas.getContext("2d");```
- Here, paintCanvas is your <canvas> element, and context is the interface that allows you to draw shapes, lines, and more.

**Drawing Paths**
- The Canvas API uses a "path-based" approach to drawing. You can think of a path as a series of connected points that the canvas "remembers."
**Key methods for paths:**
**beginPath(): Starts a new drawing path.**
**moveTo(x, y): Moves the "pen" to the starting point without drawing.**
**lineTo(x, y): Draws a straight line from the current position to the specified (x, y).**
**Applying the Drawing**
- After defining the path, you must use the stroke() method to apply it to the canvas.
**Using Coordinates**
- The (x1, y1) are the starting coordinates of the line, and (x2, y2) are the ending coordinates.
- These coordinates are relative to the canvas and should be passed into the respective moveTo() and lineTo() methods.
- 
**All the very best!**
