# root

*Community 0 | 2 files | cohesion 1.00*

## Definition

This community groups 2 file(s) rooted at `root` with dominant language py (cohesion 1.00). Central symbols: `ConsciousSystem`, `DualMind`, `HomeostasisEngine`, `LiquidNeuron`, `NestedTopoLayer`, `UnconsciousSystem`, `__init__`, `consolidate_svd`. Core file: `app.py` (29 symbols). Documented purpose: Autor: Gris Iscomeback Correo electrónico: grisiscomeback[at]gmail[dot]com Fecha de creación: xx/xx/xxxx Licencia: GPL v3  Descripción:.

## Files

| File | Language | Layer | Symbols | Doc |
|------|----------|-------|---------|-----|
| `app.py` | py | utility | 29 | yes |
| `install.sh` | sh | utility | 0 | no |

## Key Symbols

- `measure_spatial_richness` (function, `app.py:27`) `def measure_spatial_richness(activations)` - Mide diversidad de representaciones mediante eigenspectro
- `HomeostasisEngine` (class, `app.py:42`) `class HomeostasisEngine(Module)`
- `__init__` (method, `app.py:43`) `def __init__(self)`
- `decide` (method, `app.py:47`) `def decide(self, task_loss_val, richness_val, vn_entropy_val)` - Motor de decisión homeostática con targets realistas y pesos equilibrados.
- `LiquidNeuron` (class, `app.py:69`) `class LiquidNeuron(Module)` - Neurona con fast weights hebbianos (de Síntesis)
- `__init__` (method, `app.py:71`) `def __init__(self, in_dim, out_dim)`
- `forward` (method, `app.py:79`) `def forward(self, x, plasticity_gate)` - Neurona con plasticidad hebbiana de fast weights y decaimiento activación.
- `consolidate_svd` (method, `app.py:101`) `def consolidate_svd(self, repair_strength)` - Consolidación mediante SVD (modo sueño)
- `ConsciousSystem` (class, `app.py:120`) `class ConsciousSystem(Module)` - Sistema de control ejecutivo que opera sobre representaciones
- `__init__` (method, `app.py:125`) `def __init__(self, unconscious_dim, d_hid, d_out)`
- `forward` (method, `app.py:148`) `def forward(self, unconscious_features, plasticity_gate)` - Input: Representaciones del sistema inconsciente [batch, unconscious_dim]
- `get_structure_entropy` (method, `app.py:169`) `def get_structure_entropy(self)` - Análisis de salud estructural mediante SVD
- `NestedTopoLayer` (class, `app.py:183`) `class NestedTopoLayer(Module)` - Capa de procesamiento topológico con memoria episódica.
- `__init__` (method, `app.py:188`) `def __init__(self, in_dim, hid_dim, num_nodes)`
- `forward` (method, `app.py:200`) `def forward(self, x_nodes, plasticity_gate)` - x_nodes: [batch, num_nodes, in_dim]
- `get_topology_density` (method, `app.py:221`) `def get_topology_density(self)` - Densidad de conexiones topológicas
- `UnconsciousSystem` (class, `app.py:229`) `class UnconsciousSystem(Module)` - Sistema inconsciente: Procesamiento automático y paralelo.
- `__init__` (method, `app.py:234`) `def __init__(self, in_channels, grid_size, hidden_dim)`
- `forward` (method, `app.py:258`) `def forward(self, x, plasticity_gate)` - x: [batch, 3, 32, 32]
- `get_topology_stats` (method, `app.py:276`) `def get_topology_stats(self)` - Estadísticas de topología del sistema inconsciente
- `DualMind` (class, `app.py:291`) `class DualMind(Module)` - Sistema dual de procesamiento:
- `__init__` (method, `app.py:297`) `def __init__(self, in_channels, grid_size, hidden_dim, conscious_dim, num_classe`
- `forward` (method, `app.py:317`) `def forward(self, x, mode)` - Modos de operación:
- `get_system_status` (method, `app.py:343`) `def get_system_status(self)` - Diagnóstico completo del sistema dual
- `train_dualmind_phase1` (method, `app.py:358`) `def train_dualmind_phase1(model, train_loader, optimizer, device, epochs)` - FASE 1: Preentrenamiento del sistema inconsciente
- `train_dualmind_phase2` (method, `app.py:413`) `def train_dualmind_phase2(model, train_loader, optimizer, device, epochs)` - FASE 2: Entrenamiento del sistema consciente
- `train_dualmind_phase3` (method, `app.py:499`) `def train_dualmind_phase3(model, train_loader, optimizer, device, epochs)` - FASE 3: Co-adaptación de ambos sistemas
- `evaluate_dualmind` (method, `app.py:591`) `def evaluate_dualmind(model, test_loader, device)` - Evaluación del sistema dual
- `run_dualmind_experiment` (method, `app.py:616`) `def run_dualmind_experiment()`

## Internal vs External Edges

- Internal resolved imports (EXTRACTED): 0
- Cross-boundary resolved imports (EXTRACTED): 0

## Connections

- No cross-community bridges recorded. This community is self-contained.

## Risks

- No scoped security, taint, cycle, or layer risks.

## Open Questions

- Why do 1 file(s) lack file-level docs (e.g. `install.sh`)? What purpose do they serve?
- What would break if the most connected file in root changed?
- Should root be split, given cohesion 1.00?

## Sources

- `app.py`
- `install.sh`
