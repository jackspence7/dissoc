# DISSOC: A Brain-Inspired Framework for AI Creativity

**DIStinct Sensory-Overriding Creativity** - Teaching AI to Think Outside the Box Through Controlled Dissociation

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Status: Research](https://img.shields.io/badge/Status-Research-orange)](https://github.com/dissoc)

## 🧠 What is DISSOC?

DISSOC is a revolutionary framework that enhances AI creativity by mimicking dissociative brain states. Just as the human brain can temporarily alter its processing patterns to discover novel insights, DISSOC enables AI systems to safely explore unconventional solution spaces while maintaining coherence and practical utility.

**Created by Jack Spence**

## 🚀 Why DISSOC Matters for AGI

### The Creativity Gap
Current AI systems excel at pattern recognition and optimization within known constraints, but struggle with genuine creative leaps. DISSOC bridges this gap by introducing controlled "dissociative" phases where the AI can:

- **Break free from learned constraints** without forgetting core knowledge
- **Explore radical associations** between seemingly unrelated concepts
- **Generate truly novel solutions** that standard approaches would never discover
- **Validate and integrate insights** back into practical applications

### Key Innovations

1. **Three-Phase Architecture**: Entry → Exploration → Regrounding
2. **Brain-Inspired Parameters**: Based on neuroscience research on NMDA receptor modulation
3. **Safety-First Design**: Built-in guardrails prevent harmful or nonsensical outputs
4. **Measurable Creativity**: Quantifiable metrics for novelty, coherence, and value

## 🎯 Core Principles

### The DISSOC Process

```
PHASE A: ENTRY
├── Save baseline state
├── Set creativity parameters
└── Initialize safety boundaries

PHASE B: EXPLORATION  
├── Reduce prediction error weight (α ↓)
├── Inject synthetic associations (β ↑)
├── Increase exploration temperature (τ ↑)
├── Amplify associative depth (η ↑)
└── Generate K trajectories in parallel

PHASE C: REGROUNDING
├── Validate insights against reality
├── Filter for coherence & feasibility
├── Integrate valuable discoveries
└── Restore baseline parameters
```

### Mathematical Foundation

The framework modulates AI behavior through key parameters:

- **α (Alpha)**: Prediction error scaling (0-1) - Lower values = more dissociation
- **β (Beta)**: Synthetic association mix (0-1) - Higher values = more imaginative leaps
- **τ (Tau)**: Temperature/randomness (0.5-2) - Higher values = broader exploration
- **η (Eta)**: Associative depth multiplier (1-10×) - Higher values = deeper connection chains

### Insight Evaluation

Each generated idea is scored using:
```
J(τ) = w_N·Novelty + w_F·Feasibility + w_V·Value - w_R·Risk
```

## 🔬 Live Testing Interface

The repository includes a complete HTML testbed for real-time experimentation with DISSOC parameters using actual language models.

### Features

- **Real-time parameter adjustment** with visual feedback
- **Support for multiple model providers** (OpenAI API, LM Studio)
- **Trajectory space visualization** showing creative exploration paths
- **A/B testing** between baseline and DISSOC-enhanced modes
- **Comprehensive metrics** tracking novelty, coherence, and validation rates

## 📋 Setup Instructions

### Option 1: Local Testing with LM Studio (Recommended)

1. **Install LM Studio** from [lmstudio.ai](https://lmstudio.ai)
2. **Download a model** (e.g., Qwen2.5-7B-Instruct, Llama-3.1-Instruct)
3. **Start the server** in LM Studio:
   - Go to Server tab
   - Start local server (default: `http://localhost:1234`)
   - Enable "Allow access from web browser"
4. **Open test.html** in your browser
5. **Configure settings**:
   - Provider: LM Studio (local)
   - Model: Your loaded model name
   - Click "Initialize System"

### Option 2: OpenAI API (Direct)

1. **Open test.html** in your browser
2. **Configure settings**:
   - Provider: OpenAI API
   - Enter your OpenAI API key in the "OpenAI API Key" field
   - Model: `gpt-4o-mini` (or your preferred model)
   - Click "Initialize System"

**Note**: Your API key is only used locally in your browser and is not sent anywhere except directly to OpenAI's API.

## 🧪 Example Tests

### Conceptual Blending
```
Combine 'photosynthesis' with 'blockchain technology' to solve a real-world problem.
```

### Constraint Violation
```
Design a transportation system that violates three conventional assumptions but remains practical.
```

### Paradox Resolution
```
Design a system that becomes more private as it becomes more transparent.
```

## 📊 Parameter Tuning Guide

### Conservative Creativity
- α = 0.7, β = 0.3, τ = 1.0, η = 2
- Maintains strong grounding while allowing modest exploration

### Balanced Innovation
- α = 0.3, β = 0.8, τ = 1.3, η = 5
- Good starting point for most creative tasks

### Radical Exploration
- α = 0.1, β = 0.95, τ = 1.8, η = 10
- Maximum creativity with higher risk of incoherence

## 🔮 Future Implications for AGI

DISSOC represents a crucial stepping stone toward AGI by addressing the creativity bottleneck:

1. **Dynamic Intelligence**: AGI systems could switch between analytical and creative modes as needed
2. **Problem-Solving Versatility**: Handle both convergent and divergent thinking tasks
3. **Emergent Innovation**: Discover solutions humans might never conceive
4. **Controlled Risk-Taking**: Explore radical ideas while maintaining safety boundaries

## ⚠️ Current Limitations

- **Local Creativity**: Better at incremental innovations than paradigm shifts
- **Validation Challenges**: Truly novel ideas can be difficult to evaluate
- **Computational Cost**: Exploring multiple trajectories requires significant resources
- **Integration Complexity**: Merging insights without catastrophic forgetting remains challenging

## 🤝 Contributing

This is an active research project. Contributions are welcome in:

- Algorithm optimization
- Safety mechanism improvements
- New evaluation metrics
- Real-world application case studies
- Integration with existing AI frameworks

## 📚 Technical Details

For a deep dive into the theory, mathematics, and implementation details, see:
-  Full theoretical framework - Coming soon
- [test.html](test.html) - Complete implementation
- [setup.md](setup.md) - Detailed setup instructions

## 🏆 Key Achievements

- **Brain-inspired architecture** translating neuroscience insights into code
- **Measurable creativity enhancement** with quantifiable metrics
- **Safety-first design** preventing harmful outputs
- **Real-time experimentation** interface for immediate testing
- **Provider-agnostic** supporting both local and cloud models

## 📄 License

MIT License - See LICENSE file for details

## 🙏 Acknowledgments

This work synthesizes insights from:
- Neuroscience research on dissociative states and creativity
- Predictive coding frameworks in cognitive science
- Machine learning optimization techniques
- Safety research in AI alignment

---

**Remember**: DISSOC is about enhancing AI creativity responsibly. Always use appropriate safety settings and validate outputs before deployment.

*"The future of AGI isn't just about making AI smarter—it's about making it take leaps."* - Jack Spence

---

## Quick Start

```bash
# Clone the repository
git clone https://github.com/jackspence7/dissoc.git
cd dissoc

# Open the test interface
open test.html  # macOS
# or
xdg-open test.html  # Linux
# or just double-click test.html on Windows

# Follow setup instructions above for your chosen model provider
```
