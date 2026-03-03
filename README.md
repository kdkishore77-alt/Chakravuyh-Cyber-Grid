# Chakravyuh Containment for Cyber-Grid

[![Python 3.8+](https://img.shields.io/badge/python-3.8+-blue.svg)](https://www.python.org/downloads/)
[![NetworkX](https://img.shields.io/badge/NetworkX-2.5+-orange)](https://networkx.org/)

A topological approach to cyber-grid resilience inspired by the ancient Chakravyuh formation—achieving **121.8% higher multiplex resilience** than flat networks while surpassing scale-free performance **without creating vulnerable hubs**.

## 📊 Key Results

| Topology | Random Attack | Targeted Attack | Symmetry | Max Degree |
|----------|--------------|-----------------|----------|------------|
| Flat Random | 0.474 | 0.345 | 0.948 | 12 |
| Scale-Free | 0.500 | 0.290 | 0.580 | 43 |
| **Chakravyuh (Static)** | **0.500** | **0.500** | **1.000** | **22** |
| **Chakravyuh (Spiral)** | **0.487** | **0.500** | **0.974** | **6** |

**Multiplex Advantage:** Spiral Chakravyuh achieves **+121.8%** higher percolation threshold vs. flat networks in interdependent cyber-control-physical grids.

## 🔬 Core Insight

Traditional reliability creates hubs (scale-free)—creating single points of failure. Chakravyuh uses **topological containment**: layered rings with controlled radial gateways that elevate the minimum compromise fraction required for destabilization.

> *"Sacrificial outer layers, reinforced middle rings, dense protected core—with spiral paths easier to enter than exit."*

## 🏗️ Architecture

### Three-Layer Multiplex Model
- **Cyber Layer** – Edge network (first compromised)
- **Control Layer** – Intermediate dependencies  
- **Physical Layer** – Critical infrastructure (final impact)

### Topology Variants
- **Static Chakravyuh**: Concentric rings with density gradient (0.08→0.6) and radial gateways
- **Spiral Chakravyuh**: Directed inward bias (0.75) with limited outward escape—historically inspired

## 🚀 Quick Start

```python
from chakravyuh import MultiplexGrid, ContainmentExperiment

# Build three-layer Chakravyuh multiplex
builder = MultiplexGrid(n_per_layer=150)
multiplex = builder.build_chakravyuh_spiral_multiplex(layers=5)

# Evaluate cascade resilience
experiment = ContainmentExperiment(n=150)
results = experiment.evaluate_multiplex(multiplex, "Spiral Chakravyuh")

print(f"Percolation threshold: {results['percolation_threshold']:.3f}")
