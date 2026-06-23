
---

## ⚙️ System Architecture

The system is composed of three main components:

1. **SDM Workflow (Notebook)**
   - Data preprocessing
   - Environmental variable selection
   - Model training and evaluation

2. **Provenance Capture Layer**
   - Automatic logging of:
     - Inputs and parameters
     - Function calls
     - Intermediate outputs
     - Final results

3. **MongoDB Storage Layer**
   - Stores provenance records as documents
   - Enables flexible querying of workflow lineage

---

## 🗄️ MongoDB Schema

The provenance model is stored in a document-oriented structure:

- **Run document**
  - Execution ID
  - Timestamp
  - User/session metadata

- **Step document**
  - Operation type (e.g., preprocessing, modeling)
  - Input datasets
  - Parameters
  - Output artifacts

- **Lineage links**
  - Parent-child relationships between steps
  - Full traceability of transformations

See `/schema/` for detailed schema definitions.

---

## 🚀 Getting Started

### 1. Clone repository

```bash
git clone https://github.com/<your-username>/<repo-name>.git
cd <repo-name>
