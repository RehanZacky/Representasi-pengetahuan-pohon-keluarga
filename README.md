# Representasi-pengetahuan-pohon-keluarga
# Code
```python
import matplotlib.pyplot as plt
import networkx as nx

G = nx.DiGraph()

nodes = {
    "Hadi": (0, 4), "Retno": (2, 4),
    "Bayu": (-2, 3), "Desi": (0, 3), "Wahyu": (2, 3),
    "Rina": (4, 3), "Ardi": (6, 3),
    "Fahrul": (-2, 2), "Tari": (0, 2), "Nurul": (1, 2),
    "Yanto": (3, 2), "Hamzah": (5, 2),
    "Eka": (4, 2), "Mira": (6, 2), "Bastian": (7, 2),
    "Wanda": (-2, 1), "Aji": (1, 1), "Gunawan": (3, 1),
    "Anggun": (5, 1), "Boy": (7, 1)
}

for name, pos in nodes.items():
    G.add_node(name, pos=pos)

edges = [
    ("Hadi", "Bayu"), ("Hadi", "Desi"), ("Hadi", "Wahyu"), ("Hadi", "Rina"), ("Hadi", "Ardi"),
    ("Retno", "Bayu"), ("Retno", "Desi"), ("Retno", "Wahyu"), ("Retno", "Rina"), ("Retno", "Ardi"),
    ("Bayu", "Fahrul"), ("Desi", "Tari"), ("Desi", "Nurul"),
    ("Wahyu", "Yanto"), ("Rina", "Hamzah"),
    ("Eka", "Anggun"), ("Mira", "Boy"), ("Ardi", "Bastian"),
    ("Fahrul", "Wanda"), ("Nurul", "Aji"), ("Yanto", "Gunawan")
]

G.add_edges_from(edges)

pos = nx.get_node_attributes(G, 'pos')

plt.figure(figsize=(10, 8))
nx.draw(G, pos, with_labels=True, node_size=3000, node_color="lightblue", font_size=10, font_weight="bold")
plt.title("Pohon Keluarga Sederhana", fontsize=14)
plt.show()

```
# Output
![download (2)](https://github.com/user-attachments/assets/5132c02e-3f08-46c3-98c1-374c53083c9f)
