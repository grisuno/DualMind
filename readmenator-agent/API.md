# API

## app.py

### measure_spatial_richness (function) `def measure_spatial_richness(activations)`
- Defined: `app.py:27`
- Doc: Mide diversidad de representaciones mediante eigenspectro

### train_dualmind_phase1 (method) `def train_dualmind_phase1(model, train_loader, optimizer, device, epochs)`
- Defined: `app.py:358`
- Doc: FASE 1: Preentrenamiento del sistema inconsciente

### train_dualmind_phase2 (method) `def train_dualmind_phase2(model, train_loader, optimizer, device, epochs)`
- Defined: `app.py:413`
- Doc: FASE 2: Entrenamiento del sistema consciente

### train_dualmind_phase3 (method) `def train_dualmind_phase3(model, train_loader, optimizer, device, epochs)`
- Defined: `app.py:499`
- Doc: FASE 3: Co-adaptación de ambos sistemas

### evaluate_dualmind (method) `def evaluate_dualmind(model, test_loader, device)`
- Defined: `app.py:591`
- Doc: Evaluación del sistema dual

### run_dualmind_experiment (method) `def run_dualmind_experiment()`
- Defined: `app.py:616`

### __init__ (method) `def __init__(self)`
- Defined: `app.py:43`

### decide (method) `def decide(self, task_loss_val, richness_val, vn_entropy_val)`
- Defined: `app.py:47`
- Doc: Motor de decisión homeostática con targets realistas y pesos equilibrados.

### __init__ (method) `def __init__(self, in_dim, out_dim)`
- Defined: `app.py:71`

### forward (method) `def forward(self, x, plasticity_gate)`
- Defined: `app.py:79`
- Doc: Neurona con plasticidad hebbiana de fast weights y decaimiento activación.

### consolidate_svd (method) `def consolidate_svd(self, repair_strength)`
- Defined: `app.py:101`
- Doc: Consolidación mediante SVD (modo sueño)

### __init__ (method) `def __init__(self, unconscious_dim, d_hid, d_out)`
- Defined: `app.py:125`

### forward (method) `def forward(self, unconscious_features, plasticity_gate)`
- Defined: `app.py:148`
- Doc: Input: Representaciones del sistema inconsciente [batch, unconscious_dim]

### get_structure_entropy (method) `def get_structure_entropy(self)`
- Defined: `app.py:169`
- Doc: Análisis de salud estructural mediante SVD

### __init__ (method) `def __init__(self, in_dim, hid_dim, num_nodes)`
- Defined: `app.py:188`

### forward (method) `def forward(self, x_nodes, plasticity_gate)`
- Defined: `app.py:200`
- Doc: x_nodes: [batch, num_nodes, in_dim]

### get_topology_density (method) `def get_topology_density(self)`
- Defined: `app.py:221`
- Doc: Densidad de conexiones topológicas

### __init__ (method) `def __init__(self, in_channels, grid_size, hidden_dim)`
- Defined: `app.py:234`

### forward (method) `def forward(self, x, plasticity_gate)`
- Defined: `app.py:258`
- Doc: x: [batch, 3, 32, 32]

### get_topology_stats (method) `def get_topology_stats(self)`
- Defined: `app.py:276`
- Doc: Estadísticas de topología del sistema inconsciente

### __init__ (method) `def __init__(self, in_channels, grid_size, hidden_dim, conscious_dim, num_classes)`
- Defined: `app.py:297`

### forward (method) `def forward(self, x, mode)`
- Defined: `app.py:317`
- Doc: Modos de operación:

### get_system_status (method) `def get_system_status(self)`
- Defined: `app.py:343`
- Doc: Diagnóstico completo del sistema dual
