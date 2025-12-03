# LearnCurve 📈

**An interactive visualization of how neural networks learn**

Watch a neural network learn to approximate any mathematical function in real-time. No installation required – runs entirely in your browser!

## 🎯 Try It Now

**[Launch LearnCurve →](https://rowenchris.github.io/MLdemo/)**

---

## What You'll See

| Panel | Description |
|-------|-------------|
| **Network Design** | Animated diagram showing neurons, weights, and biases |
| **Fit Plot** | Green target f(x) vs blue prediction ŷ(x) |
| **Training Trace** | Loss curve with rolling average |
| **Loss Landscape** | 2D heatmap showing optimization path |

**Goal:** Make blue match green by training the network!

---

## ✨ Features

### 🎮 Interactive Controls
- **Target Function**: Type any math expression (`x*x`, `sin(x)`, `abs(x)`, `x^3-x`, etc.)
- **Learning Rate**: Control step size (0.001 to 0.5)
- **Optimizer**: Compare Simple (SGD) and Adam algorithms
- **Noise**: Test robustness with noisy training data
- **Activation**: Choose between ReLU and Sigmoid

### 🧠 Network Design
- Adjust hidden layers (1-4) and neurons per layer (2-16)
- Drag handles for quick architecture changes
- Watch weights and biases update in real-time
- See total parameter count

### 📊 Visualization
- **Fit Plot**: Prediction curve approaching target with sample points
- **Training Trace**: Loss over time with rolling average and ΔLoss indicator
- **Loss Landscape**: 2D visualization of loss surface with optimization trail
- **Equations Panel**: Forward pass and backpropagation math explained

### 🔬 Comparison Mode
- Save two training runs (A & B) with different settings
- Compare learning curves side-by-side
- Discover: Which configuration learns faster?

### 📸 Capture
- **Screenshot**: Download PNG of current state (works offline)
- **Animated GIF**: Record training convergence (requires web server)

### ⏸️ Smart Features
- **Auto-pause**: Stops when training converges (loss stops decreasing)
- **Zoom**: Drag handle to focus on early training steps
- **Gradient clipping**: Prevents numerical instability

---

## 🎓 Who Is This For?

Students learning machine learning who have:
- ✅ Basic algebra and function notation
- ✅ Familiarity with calculus (derivatives, chain rule)
- ✅ Curiosity about how AI learns!

### Concepts Demonstrated
1. **Forward Pass** – How inputs flow through layers
2. **Loss Function** – Measuring prediction error (MSE)
3. **Backpropagation** – Computing gradients via chain rule
4. **Gradient Descent** – Adjusting weights to minimize loss
5. **Optimization** – How Adam outperforms simple SGD
6. **Loss Landscape** – Visualizing the optimization surface

---

## 🧪 Suggested Experiments

| Experiment | What You'll Learn |
|------------|-------------------|
| Train on `x*x` | Basic quadratic fitting |
| Try `sin(x)` | Networks can learn periodic functions |
| Compare `x^3` vs `x^3-x` | Complexity affects learning |
| Add noise (0.3) | Robustness to noisy data |
| Compare Adam vs Simple | Why adaptive optimizers help |
| 1 layer vs 4 layers | Depth vs training speed trade-off |
| 3 neurons vs 16 neurons | Width vs expressiveness |
| Watch Loss Landscape | See gradient descent in action |

---

## 🚀 Running Locally

### Quick Start (Screenshot only)
Just open `index.html` in your browser!

### Full Features (with GIF capture)
```bash
cd MLdemo
python3 -m http.server 8000
# Open http://localhost:8000
```

---

## 🛠️ Technical Details

- **Pure HTML/CSS/JavaScript** – zero dependencies
- **No build step** – single self-contained file
- **~4000 lines** of code
- **Responsive design** – works on mobile and desktop
- **Gradient clipping** – numerically stable training

---

## 🤝 Credits

Built by **Chris Rowen** and **Claude Opus 4** (Anthropic)

---

## 📄 License

[MIT License](LICENSE) – Use, modify, and share freely!

Copyright © 2025 Chris Rowen

---

⭐ **Star this repo if you find it useful for teaching or learning!**
