# Interactive Bézier Rope

## Overview
This project visualizes an interactive cubic Bézier curve that behaves like a flexible rope. The curve responds smoothly to mouse movement using spring-based physics applied to the control points.

## Math Model
The rope is represented using a **cubic Bézier curve** defined by four points:

- P0, P3 → fixed endpoints
- P1, P2 → dynamic control points

The Bézier curve is computed as:

B(t) = (1−t)³P0 + 3(1−t)²tP1 + 3(1−t)t²P2 + t³P3,  
where t ∈ [0,1].

Tangents are calculated using the derivative of the Bézier equation and normalized for visualization.

## Physics Model
Control points P1 and P2 follow **spring–damper physics**:

- Spring force pulls the point toward a target position
- Damping reduces oscillations

This creates smooth, elastic motion similar to a rope or cable.

Constants:
- Spring constant = 0.02
- Damping factor = 0.85

## Interaction
- Mouse movement updates target positions of control points
- Curve reacts dynamically in real time

## Design Choices
- HTML Canvas for real-time rendering
- JavaScript for physics and math calculations
- Lightweight, dependency-free implementation

## How to Run
Simply open `index.html` in a browser.
