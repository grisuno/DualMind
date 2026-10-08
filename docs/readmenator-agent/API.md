# API

## app.py
- `measure_spatial_richness` (function) `app.py:27` `def measure_spatial_richness(activations)` -- Mide diversidad de representaciones mediante eigenspectro
- `HomeostasisEngine.__init__` (method) `app.py:43` `def __init__(self)`
- `HomeostasisEngine.decide` (method) `app.py:47` `def decide(self, task_loss_val, richness_val, vn_entropy_val)` -- Motor de decisión homeostática con targets realistas y pesos equilibrados. - target_entropy=1.8: Valor alcanzable...
- `LiquidNeuron.__init__` (method) `app.py:71` `def __init__(self, in_dim, out_dim)`
- `LiquidNeuron.forward` (method) `app.py:79` `def forward(self, x, plasticity_gate)` -- Neurona con plasticidad hebbiana de fast weights y decaimiento activación.
- `LiquidNeuron.consolidate_svd` (method) `app.py:101` `def consolidate_svd(self, repair_strength)` -- Consolidación mediante SVD (modo sueño)
- `ConsciousSystem.__init__` (method) `app.py:125` `def __init__(self, unconscious_dim, d_hid, d_out)`
- `ConsciousSystem.forward` (method) `app.py:148` `def forward(self, unconscious_features, plasticity_gate)` -- Input: Representaciones del sistema inconsciente [batch, unconscious_dim] Output: logits, métricas homeostáticas
- `ConsciousSystem.get_structure_entropy` (method) `app.py:169` `def get_structure_entropy(self)` -- Análisis de salud estructural mediante SVD
- `NestedTopoLayer.__init__` (method) `app.py:188` `def __init__(self, in_dim, hid_dim, num_nodes)`
- `NestedTopoLayer.forward` (method) `app.py:200` `def forward(self, x_nodes, plasticity_gate)` -- x_nodes: [batch, num_nodes, in_dim] output: [batch, num_nodes, hid_dim]
- `NestedTopoLayer.get_topology_density` (method) `app.py:221` `def get_topology_density(self)` -- Densidad de conexiones topológicas
- `UnconsciousSystem.__init__` (method) `app.py:234` `def __init__(self, in_channels, grid_size, hidden_dim)`
- `UnconsciousSystem.forward` (method) `app.py:258` `def forward(self, x, plasticity_gate)` -- x: [batch, 3, 32, 32] output: [batch, output_dim] representaciones inconscientes
- `UnconsciousSystem.get_topology_stats` (method) `app.py:276` `def get_topology_stats(self)` -- Estadísticas de topología del sistema inconsciente
- `DualMind.__init__` (method) `app.py:297` `def __init__(self, in_channels, grid_size, hidden_dim, conscious_dim, num_classes)`
- `DualMind.forward` (method) `app.py:317` `def forward(self, x, mode)` -- Modos de operación: - 'unconscious': Solo sistema inconsciente (rápido, baseline) - 'conscious': Consciente sobre...
- `DualMind.get_system_status` (method) `app.py:343` `def get_system_status(self)` -- Diagnóstico completo del sistema dual
- `DualMind.train_dualmind_phase1` (method) `app.py:358` `def train_dualmind_phase1(model, train_loader, optimizer, device, epochs)` -- FASE 1: Preentrenamiento del sistema inconsciente Objetivo: Aprender representaciones topológicas ricas
- `DualMind.train_dualmind_phase2` (method) `app.py:413` `def train_dualmind_phase2(model, train_loader, optimizer, device, epochs)` -- FASE 2: Entrenamiento del sistema consciente Objetivo: Aprender decisiones homeostáticas óptimas Sistema...
- `DualMind.train_dualmind_phase3` (method) `app.py:499` `def train_dualmind_phase3(model, train_loader, optimizer, device, epochs)` -- FASE 3: Co-adaptación de ambos sistemas Objetivo: Refinamiento conjunto con retroalimentación
- `DualMind.evaluate_dualmind` (method) `app.py:591` `def evaluate_dualmind(model, test_loader, device)` -- Evaluación del sistema dual
- `DualMind.run_dualmind_experiment` (method) `app.py:616` `def run_dualmind_experiment()`
