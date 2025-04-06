# Summary of Altoidsjedi's Comments on MoE Models

### Key Points About MoE Architecture

1. **Structure of Transformer Models**:
   - Traditional transformer models consist of layers with Attention → Normalization → FFNN repeated N times.
   - In dense models (e.g., a 70B parameter model), all layers use a single FFNN.

2. **MoE Model Difference**:
   - Instead of one FFNN per layer, MoE models have multiple FFNNs ("experts") per layer.
   - A routing mechanism dynamically selects one or two experts per layer for each forward pass based on the token context.

3. **Parameter Scaling**:
   - Total parameters = (non-FFNN parameters) + (FFNN parameters × number of experts).
   - Example: A model might have 400B+ total parameters, but only ~17B are active during any forward pass.

4. **Advantages**:
   - Scales capacity without proportionally increasing compute requirements during inference.
   - Improves generalization and emergent abilities.
   - Reduces memory bandwidth requirements between RAM/VRAM and CPU/GPU during inference.

5. **Disadvantages**:
   - Requires significant RAM/VRAM to store all experts, even inactive ones.

---

### Clarification on Expert Selection

1. **Dynamic Routing**:
   - Experts are chosen dynamically at every layer for every token based on context.
   - Each layer uses:
     - A shared/static FFNN (always active).
     - A dynamically selected FFNN from the pool of experts (e.g., 16 experts in LLaMA 4 Scout).

2. **Learned Parameters**:
   - Both the expert FFNN parameters and the router parameters are learned during training.

3. **Conceptual Model**:
   - Think of it as "a single ~16B model with 16 expert FFNNs added to each layer, from which one is dynamically chosen per layer during inference."

---

### Practical Example
- On a high-end desktop (e.g., Ryzen 9600X with 96GB DDR5 RAM), an int4 quantized LLaMA 4 Scout model (~55–60GB RAM) can run as fast as a dense ~17B model, despite having much higher total capacity.

---
Answer from Perplexity: pplx.ai/share
