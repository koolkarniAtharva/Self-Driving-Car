# 🚗 Self-Driving Car Simulation

<div align="center">

![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)
![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white)
![Canvas](https://img.shields.io/badge/Canvas-FF6B6B?style=for-the-badge&logo=html5&logoColor=white)

**A pure JavaScript implementation of a self-driving car using neural networks and genetic algorithms**

[Live Demo](https://selfdrivingcarwithga.netlify.app/) 

</div>

---

## 🌟 Overview

This project is a **fully functional self-driving car simulation** built from scratch using vanilla JavaScript and HTML Canvas. The car learns to navigate traffic using a neural network and evolves its behavior through a genetic algorithm with mutation. Watch as AI-controlled cars learn to avoid obstacles, stay in lane, and navigate through traffic!

## ✨ Features

### 🧠 Neural Network Brain
- Custom-built feedforward neural network implementation
- 5 sensor inputs feeding into a 6-node hidden layer
- 4 output nodes controlling car movements (forward, left, right, reverse)
- Real-time visualization of neural network activity

### 🔬 Genetic Algorithm
- Population-based learning with 100 concurrent cars
- Mutation system for exploring different driving strategies
- Best performer selection and brain preservation
- Save/load functionality using browser localStorage

### 🚦 Realistic Physics
- Accurate car movement with acceleration and friction
- Collision detection using polygon intersection
- Angle-based steering mechanics
- Speed limits and reverse capabilities

### 📡 Sensor System
- 5-ray sensor array for environment detection
- 150-pixel detection range
- Detects both road borders and traffic
- Visual ray rendering for debugging

### 🎮 Interactive Controls
- Manual control option using arrow keys
- Save best-performing brain (💾 button)
- Discard saved progress (🗑️ button)
- Real-time camera following the best car

## 🎯 How It Works

### The Learning Process

1. **Initialization**: 100 AI-controlled cars spawn at the starting position
2. **Sensing**: Each car uses 5 sensors to detect distances to obstacles
3. **Decision Making**: Neural network processes sensor data and outputs control signals
4. **Evolution**: Best-performing car's brain is saved and mutated for the next generation
5. **Iteration**: Process repeats, gradually improving driving behavior

### Neural Network Architecture

```
Input Layer (5 nodes) → Sensor readings
         ↓
Hidden Layer (6 nodes) → Processing
         ↓
Output Layer (4 nodes) → Controls [Forward, Left, Right, Reverse]
```

### Key Components

| Component | Purpose |
|-----------|---------|
| **Car** | Main vehicle class with physics and rendering |
| **Sensor** | Ray-casting system for environment detection |
| **Neural Network** | Brain that makes driving decisions |
| **Controls** | Input handling (AI or keyboard) |
| **Road** | Track rendering with multiple lanes |
| **Visualizer** | Neural network visualization |

## 🚀 Getting Started

### Prerequisites

- A modern web browser (Chrome, Firefox, Safari, Edge)
- Basic understanding of JavaScript (for customization)

### Installation

1. Clone the repository:
```bash
git clone https://github.com/koolkarniAtharva/Self-Driving-Car
cd Self-Driving-Car
```

2. Open `index.html` in your browser:
```bash
# On macOS
open index.html

# On Linux
xdg-open index.html

# On Windows
start index.html
```

Or simply drag and drop `index.html` into your browser window.

### Usage

**Training the AI:**
1. Open the simulation in your browser
2. Watch as cars attempt to navigate through traffic
3. The best-performing car (most progress) is highlighted with full opacity
4. Click 💾 to save the best brain
5. Refresh the page to continue training from the saved brain

**Manual Control:**
- Use arrow keys to control a car manually
- Modify `controlType` in `main.js` from `"AI"` to `"KEYS"`

## 📁 Project Structure

```
self-driving-car/
│
├── index.html          # Main HTML file
├── style.css           # Styling and layout
├── main.js            # Application entry point and animation loop
│
├── car.js             # Car class with physics and rendering
├── controls.js        # Input handling system
├── sensor.js          # Ray-casting sensor implementation
├── network.js         # Neural network and learning algorithms
│
├── road.js            # Road rendering and lane management
├── visualizer.js      # Neural network visualization
├── utils.js           # Helper functions (lerp, intersections, etc.)
│
└── car.png            # Car sprite image
```

## 🎨 Customization

### Adjust Population Size
```javascript
// In main.js
const N = 100; // Change to desired number of cars
```

### Modify Mutation Rate
```javascript
// In main.js - NeuralNetwork.mutate()
NeuralNetwork.mutate(cars[i].brain, 0.1); // 0.1 = 10% mutation rate
```

### Change Traffic Patterns
```javascript
// In main.js - traffic array
const traffic = [
    new Car(road.getLaneCenter(1), -100, 30, 50, "DUMMY", 2, getRandomColor()),
    // Add more traffic cars here
];
```

## 🧪 Technical Details

### No Libraries Used
This project is built entirely from scratch without any external libraries or frameworks:
- ✅ Custom neural network implementation
- ✅ Hand-coded physics engine
- ✅ Pure Canvas API rendering
- ✅ Vanilla JavaScript ES6+

### Performance Optimizations
- Efficient collision detection using polygon intersection
- Optimized rendering with alpha blending for non-best cars
- Minimal DOM manipulation
- RequestAnimationFrame for smooth 60 FPS animation

## 🤝 Contributing

Contributions are welcome! Here are some ideas:

- [ ] Add more complex traffic patterns
- [ ] Implement different neural network architectures
- [ ] Add sound effects
- [ ] Create different difficulty levels
- [ ] Add multiplayer mode
- [ ] Implement reinforcement learning


## 🙏 Acknowledgments

- Inspired by the fascinating field of neuroevolution
- Built as an educational project to understand machine learning fundamentals
- No external libraries or frameworks used - pure JavaScript implementation

---

<div align="center">

**Made with ❤️ by Atharva**

If you found this project interesting, please consider giving it a ⭐!

</div>