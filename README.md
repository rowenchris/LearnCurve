# LearnCurve 📈

**An interactive visualization of how neural networks learn to approximate functions**

Watch a neural network learn in real-time through a structured three-phase workflow. No installation required – runs entirely in your browser!

## 🎯 Try It Now

**[Launch LearnCurve →](https://rowenchris.github.io/LearnCurve/)**

---

## Three-Phase Learning Workflow

LearnCurve guides you through the machine learning process:

| Phase | What You Do |
|-------|-------------|
| **① Create Training Data** | Define a "data recipe" function, set the range and noise level, then generate training examples |
| **② Train the Model** | Configure network architecture and hyperparameters, then watch the model learn |
| **③ Evaluate & Compare** | Test on held-out data to measure generalization; save and compare different runs |

---

## What You'll See

| Panel | Description |
|-------|-------------|
| **Network Design** | Animated diagram showing neurons, weights, and biases with operation counts |
| **Examples vs Model** | Training points (blue) vs model prediction (blue curve), with optional held-out data and recipe overlay |
| **Training Trace** | Error curves (training + test) with rolling average and ΔError indicator |
| **Loss Landscape** | 2D heatmap showing loss surface with training path overlay |

**Goal:** Train the network until the blue prediction curve matches the data!

---

## ✨ Features

### 🎮 Data Generation (Phase 1)
- **Data Recipe**: Any math expression (`sin(x)`, `x^2`, `x^3-3*x`, `abs(x)`, etc.)
- **Range Control**: Set x-range for data generation
- **Noise Level**: Add realistic noise to training data
- **Train/Test Split**: Automatic 80/20 split with held-out test set

### 🧠 Network Design & Training (Phase 2)
- Adjust hidden layers (1-5) and neurons per layer (1-32)
- Unified slider controls with labeled value displays
- **Learning Rate (η)**: Control step size (0.001 to 0.5)
- **Optimizer**: Compare Simple (SGD) vs Adam
- **Activation (σ)**: Choose between ReLU and Sigmoid
- **Training Range**: Restrict training to test extrapolation
- Watch weights and biases update in real-time

### 📊 Visualization
- **Examples vs Model**: Prediction curve with training points; reveal held-out test data and original recipe
- **Training Trace**: Error over time with test error overlay and zoom control
- **Loss Landscape**: 2D heatmap showing the loss surface as a function of two selected weights
- **Equations Panel**: Forward and backward pass math explained

### 🗺️ Loss Landscape Algorithm
The loss landscape is computed using an **exploration-based algorithm**:
- **150 training runs** from a 15×10 grid of starting positions
- Each run trains for **600 steps** with all weights free to move
- **5×5 patches** are probed around start and end positions
- Results are **averaged** where runs overlap, reducing path-dependency noise
- Final **60×40 display grid** (2,400 cells) captures real structure
- Computes in **~2-3 seconds** with no intermediate UI updates

### 🔬 Evaluation & Comparison (Phase 3)
- Evaluate model on held-out test data
- See in-range vs extrapolation performance
- Save two training runs (A & B) with different settings
- Compare learning curves side-by-side

### 📖 Learning Guide
- Built-in sidebar explaining key ML concepts
- "The Big Picture" overview
- Key Terms glossary
- Math explanations (forward pass, backprop, chain rule)
- Suggested experiments

### 📸 Capture
- **Screenshot**: Download PNG of current state
- **Animated GIF**: Record training convergence

---

## 📐 Mathematical Notation

LearnCurve uses student-friendly notation aligned with standard machine learning education:

| Symbol | Meaning |
|--------|---------|
| `x` | Input value |
| `t` | Target (true value from data recipe) |
| `y` | Model prediction |
| `w_ij` | Weights to hidden layer (layer i, neuron j) |
| `w_j` | Weights to output (neuron j) |
| `b_ij` | Hidden layer biases (layer i, neuron j) |
| `b` | Output bias |
| `h_ij` | Hidden neuron activations (layer i, neuron j) |
| `z_ij` | Pre-activation (weighted sum) |
| `σ` | Activation function (ReLU or Sigmoid) |
| `E` | Error: E = ½(y − t)² |
| `η` | Learning rate |

### Forward Pass
```
z_ij = w_ij·x + b_ij    (weighted sum, hidden layer)
h_ij = σ(z_ij)          (activation)
y = w₁h₁ + w₂h₂ + ... + b  (output)
E = ½(y − t)²           (error)
```

### Backward Pass (Gradients)
```
∂E/∂y = y − t           (error derivative)
∂E/∂w_j = (∂E/∂y)·h_j   (output weight gradient)
∂E/∂h_ij = (∂E/∂y)·w_j  (hidden activation gradient)
∂E/∂z_ij = (∂E/∂h_ij)·σ'(z_ij)  (chain rule)
```

### Weight Update (SGD)
```
w ← w − η · ∂E/∂w
```

---

## 🎓 Who Is This For?

Students learning machine learning who have:
- ✅ Basic algebra and function notation
- ✅ Familiarity with calculus concepts (derivatives, chain rule)
- ✅ Curiosity about how AI learns!

### Concepts Demonstrated
1. **Training vs Test Data** – Why we hold out data for evaluation
2. **Forward Pass** – How inputs flow through layers (weighted sums + activations)
3. **Error Function** – Measuring prediction error (MSE): E = ½(y − t)²
4. **Backpropagation** – Computing gradients via chain rule
5. **Gradient Descent** – Adjusting weights to minimize error
6. **Epochs** – Multiple passes through training data
7. **Overfitting** – When models memorize instead of generalize
8. **Interpolation vs Extrapolation** – Performance inside vs outside training range

---

## 🧪 Suggested Experiments

| Experiment | What You'll Learn |
|------------|-------------------|
| Train on `sin(x)` | Networks can learn periodic functions |
| Try `x^3-3*x` | Polynomial with turning points |
| Compare `abs(x)` vs `sign(x)` | Sharp features are harder |
| Add noise (0.1) | Robustness to noisy data |
| Compare Adam vs Simple | Why adaptive optimizers help |
| 1 layer vs 4 layers | Depth vs training speed trade-off |
| 3 neurons vs 16 neurons | Width vs expressiveness |
| Restrict training range | See extrapolation failures |
| Watch Loss Landscape | See gradient descent navigate the loss surface |

---

## 🚀 Running Locally

### Quick Start
Just open `index.html` in your browser!

### With Local Server (for GIF capture)
```bash
cd MLdemo
python3 -m http.server 8000
# Open http://localhost:8000
```

---

## 🛠️ Technical Details

- **Pure HTML/CSS/JavaScript** – zero dependencies
- **No build step** – single self-contained file
- **~8000 lines** of code
- **Responsive design** – works on desktop (sidebar hidden on mobile)
- **Gradient clipping** – numerically stable training
- **Smart auto-pause** – stops training when loss improvement drops below 1% over 1000 steps
- **Optimized loss surface** – exploration algorithm with probe averaging for consistent visualization

---

## 🤝 Credits

Built by **Chris Rowen** with assistance from **Claude** (Anthropic)

---

## 📄 License

[MIT License](LICENSE) – Use, modify, and share freely!

Copyright © 2025 Chris Rowen

---

⭐ **Star this repo if you find it useful for teaching or learning!**
