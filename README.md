# Provenance-Aware Species Distribution Modeling with MongoDB

This repository provides a reproducible implementation of a provenance-aware workflow for Species Distribution Modeling (SDM), integrating Jupyter Notebooks with a MongoDB backend to automatically capture, store, and query computational provenance.

The system is designed to enhance transparency, reproducibility, and reusability of ecological modeling workflows, particularly in spatial biodiversity studies.

---

## 📌 Overview

The workflow implements an SDM pipeline with integrated provenance tracking, including:

- Automated provenance capture during notebook execution
- Storage of execution traces in MongoDB
- Schema design for representing SDM workflows
- Query system for retrieving computational lineage
- Examples of provenance queries for analysis and auditing

This approach enables full traceability of data inputs, transformations, and model outputs.

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

