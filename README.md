# Hash Table Performance Benchmark

A high-performance C++ benchmarking tool designed to evaluate and compare different hash table collision resolution strategies.

## 🚀 Implemented Structures
This project features three distinct custom hash table implementations:
1. **Separate Chaining (Singly Linked List):** Classic chaining using a custom-built singly linked list structure.
2. **Separate Chaining (AVL Tree):** Advanced collision resolution utilizing self-balancing AVL trees within buckets.
3. **Open Addressing (Linear Probing):** Flat array structure with linear probing for collision handling.

## ⚙️ Features & Capabilities
* **Interactive CLI Interface:** Allows manual execution and testing of core operations (`Insert`, `Remove`, `Find`, `Load from file`, `Generate random`, `Display`, `Clear`).
* **Automated Benchmarking Suite:** Measures the average execution time of `insert()` and `remove()` operations across various data scales with nanosecond precision.

## 🔬 Benchmarking Methodology
The built-in benchmark (Menu Option 4) is designed for rigorous average-case performance analysis:
* **Data Scales:** Tests across 8 different structure sizes, ranging from 5,000 to 100,000 elements.
* **Reproducibility:** Uses 10 fixed (deterministic) generator seeds for each dataset size. The final result is averaged across these 10 runs to approximate the average-case scenario.
* **Isolated Measurement:** Each operation is measured on a separate, fresh copy of the structure. This ensures the structure's size remains strictly constant during the actual time measurement.
* **Fair Comparison:** All three hash table variants are tested against the exact same input datasets.
* **Data Export:** Results are automatically exported to CSV format (using `;` delimiter) for easy data visualization: 
  * `results/insert_times.csv`
  * `results/remove_times.csv`

## 🛠️ Build & Run Instructions
The project is built using CMake. A `Release` build is strongly recommended to ensure accurate performance measurements.

```bash
mkdir build
cd build
cmake -DCMAKE_BUILD_TYPE=Release ..
make
./projekt
