# LearnCurve 📈

**An interactive visualization of how neural networks learn**

Watch a neural network learn to approximate any mathematical function in real-time. No installation required – runs entirely in your browser!

## 🎯 Try It Now

**[Launch LearnCurve →](https://YOUR_USERNAME.github.io/LearnCurve/)**

*(Update this link after deployment)*

---

## What You'll See

| Green Curve | Blue Curve |
|-------------|------------|
| Target function f(x) | Network's prediction ŷ(x) |
| What we want to learn | What the network currently outputs |

**Goal:** Make blue match green by training the network!

---

## ✨ Features

### 🎮 Interactive Controls
- **Target Function**: Type any math expression (`x*x`, `sin(x)`, `abs(x)`, etc.)
- **Learning Rate**: Control step size (bigger = faster but unstable)
- **Optimizer**: Compare Simple, Momentum, and Adam algorithms
- **Noise**: Test robustness with noisy training data

### 🧠 Network Design
- Adjust hidden layers (1-3) and neurons (2-10)
- Switch activation functions (ReLU, Tanh, Sigmoid)
- Watch weights update in real-time

### 📊 Visualization
- **Fit Plot**: Prediction curve approaching target
- **Training Trace**: Loss decreasing over time
- **Equations**: The math behind forward pass & backpropagation

### 🔬 Comparison Mode
- Save two training runs with different settings
- Compare learning curves side-by-side
- Discover: Which configuration learns faster?

---

## 🎓 Who Is This For?

Students learning machine learning who have:
- ✅ Basic algebra
- ✅ Familiarity with calculus (chain rule)
- ✅ Curiosity about how AI learns!

### Concepts Demonstrated
1. **Forward Pass** – How inputs flow through the network
2. **Loss Function** – Measuring prediction error
3. **Backpropagation** – Computing gradients via chain rule
4. **Gradient Descent** – Adjusting weights to minimize loss

---

## 🧪 Suggested Experiments

| Experiment | What You'll Learn |
|------------|-------------------|
| Train on `x*x` | Basic quadratic fitting |
| Try `sin(x)` | Networks can learn periodic functions |
| Add noise (0.3) | Robustness to noisy data |
| Compare Adam vs Simple | Why adaptive optimizers help |
| 1 layer vs 3 layers | Depth vs training speed |

---

## 🛠️ Technical Details

- **Pure HTML/CSS/JavaScript** – zero dependencies
- **No build step** – just open the file
- **~3000 lines** of self-contained code
- **Works on mobile** and desktop browsers

---

## 🤝 Credits

Built by **Chris Rowen** and **Claude 4.5 Opus** (Anthropic)

---

## 📄 License

MIT License – Use, modify, and share freely!

---

⭐ **Star this repo if you find it useful for teaching or learning!**
