# zoran-latence-énergie

**Module d’instrumentation et d’optimisation** pour l’écosystème Zoran / QuantaGlottal©® — suivi de la latence (µs) et de la consommation énergétique (J), avec détection automatique des régressions.

---

## ✨ Fonctionnalités
- **Mesure de latence** à la microseconde
- **Mesure de consommation énergétique** en Joules
- **Budgets cibles** configurables par type d’opération
- **Rapports détaillés** par exécution (JSON, CSV, Markdown)
- **Détection de régression** automatique avec seuils d’alerte
- **Intégration CI/CD** pour blocage si dépassement

---

## 📦 Installation (développement)
```bash
pip install -e .


---

⚡ Exemple rapide

from zoran_latence_energie import Profiler

profiler = Profiler(budget_latency_us=500, budget_energy_j=0.05)

with profiler.measure("injection"):
    # Code à mesurer
    result = heavy_operation()

report = profiler.generate_report()
print(report)

if profiler.detect_regression(report):
    print("⚠ Régression détectée")


---

🧱 Structure suggérée

src/zoran_latence_energie/
  __init__.py
  profiler.py          # mesures temps + énergie
  budgets.py           # définition et contrôle
  reporting.py         # génération de rapports
  regression.py        # détection d'anomalies
tests/
  test_profiler.py
pyproject.toml
.gitignore
LICENSE
README.md


---

🧪 Tests

pytest -q


---

🔐 Éthique

Le zoran-latence-énergie applique :

le principe vivant > humain

l’optimisation énergétique avant la performance brute

la transparence sur l’empreinte de chaque action



---

📜 Licence

MIT — voir LICENSE.


---

Auteur : Frédéric Tabary — Institut IA
Contact : 0645605023 — Canada, Montréal, France
INSTITUT🦋 IA INC., 7100-380, rue Saint-Antoine Ouest, Montréal (Québec) H2Y 3X7.# zoran-latency-energy
Instrumentation (µs, J) + budgets; rapports par run, régression détectée automatiquement.
