# 🛠️ Bedretto Ontology

The **Bedretto Ontology** provides structured semantic definitions for boreholes, core samples, sensors, monitoring systems, and geological metadata, as used at the [Bedretto Underground Laboratory for Geosciences and Geoenergies](https://bedrettolab.ethz.ch), which are also applicable to other underground facilites.

📄 **Documentation:** [https://sdsc-ordes.github.io/bedretto-ontology/](https://sdsc-ordes.github.io/bedretto-ontology/)

---

## 🧠 Overview

This ontology models geoscientific infrastructure and observations. It supports data integration, documentation, and interoperability for subsurface research, particularly in the context of experimental test beds and monitoring boreholes.

**Key concepts include:**

- **Boreholes**: Physical shafts drilled into the ground.
- **Core & Core Samples**: Extracted geological materials and their descriptions.
- **Downhole Logging**: Recorded physical and geological data from within boreholes.
- **Sensors**: Including seismic, hydraulic, hydromechanical, and fibre-optic types.
- **Monitoring & Configuration**: Observation setups and sensor parameterization.
- **Geology**: Descriptive metadata for geological structures.
- **Test Beds**: Experimental sites and their purpose.

The ontology is modular and extendable, with a focus on real-world operational workflows and sensor installations.

---

## 📁 Repository Structure
```yaml
.
├── .github/workflows # GitHub Actions: CI for checks and docs
│ ├── checks.yaml
│ └── docs.yaml
├── README.md # You're reading it
├── docs/ # Rendered documentation & diagrams
│ ├── index.html
│ └── BoreholeDB_v0.1_relationships.PNG
├── external/ # Source vocabularies and domain references
│ ├── BoreholeDB_v0.1.accdb
│ ├── BoreholeIE_consolidated_vocab_ed.xlsx
│ └── Borehole_consolidated_vocab_02.xlsx
├── ontology/ # Core ontology (Turtle format)
│ └── bedretto-ontology.ttl
├── src/quality-checks/ # SHACL shapes for validation
│ └── shacl-shacl.ttl
└── tools/python/ # Python tools for SHACL and SPARQL
├── checks/shacl.py
├── docs/sparql.py
└── requirements.txt
```
## 🧪 Continuous Integration

This repository includes a GitHub Actions pipeline that automatically:

- ✅ **Validates** the ontology with SHACL (`checks.yaml`)
- 🧾 **Regenerates** HTML documentation from the ontology (`docs.yaml`)

All changes to the ontology file or shapes will trigger these checks automatically when committed.

---

## ✍️ How to Contribute

Want to propose changes or additions to the ontology? Here's how:

1. **Edit the Ontology**

   Open and modify:  
   `ontology/bedretto-ontology.ttl`

2. **(Optional) Add or Update SHACL Shapes**

   For quality checks or structure enforcement, modify:  
   `src/quality-checks/shacl-shacl.ttl`

3. **Run Local Validation (optional)**

   To validate your changes before committing:
   ```bash
   pip install -r tools/python/requirements.txt
   python tools/python/checks/shacl.py
Commit Your Changes

```bash
git add ontology/bedretto-ontology.ttl
git commit -m "Describe your ontology update"
git push
```
CI Will Run Automatically

GitHub will validate the ontology and regenerate the documentation.
Once merged, the updated docs are available at:
👉 https://sdsc-ordes.github.io/bedretto-ontology/

👥 Contributors

- [Liliana Vargas](https://github.com/anailil)
- [Robin Franken](https://github.com/rmfranken/) (With contributions and stewardship by the Bedretto Lab, ETH Zurich)
