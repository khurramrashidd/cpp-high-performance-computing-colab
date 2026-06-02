# 🌀 Polyglot C++ Fractal Engine in Colab

A high-performance computing (HPC) demonstration showcasing native C++ execution within a Google Colab/Jupyter Notebook environment. This project builds a functional Mandlebrot fractal engine in C++, compiles it into a native binary, and executes it directly on the underlying Linux OS to deliver massive CPU-level optimization.

Python is strategically deployed as a lightweight presentation layer to visualize the final output, creating a true polyglot developer workflow.

## 🌟 Features

* **Native C++ Performance:** Executes all complex mathematical iterations and file I/O using native C++, bypassing the overhead of interpreted languages like Python for heavy arithmetic.
* **Compiler Optimization (`-O3`):** Demonstrates how to leverage standard Linux toolchains (`g++`) to compile an optimized binary that maximizes CPU core throughput.
* **Polyglot Architecture:** Seamlessly orchestrates three distinct developer languages:
  1. **C++ (HPC Engine):** For intense Mandelbrot computation and PPM file generation.
  2. **Bash (System Glue):** For compilation, system-level execution, and direct interaction with the OS.
  3. **Python (Visualization Layer):** For reading the native output file (`.ppm`) and rendering the result.

## 🛠️ Tech Stack

* **Language (HPC Engine):** C++
* **System/Execution Interface:** Bash
* **Language (Visualization):** Python
* **Key Libraries:** `<complex>`, `<iostream>`, `<fstream>` (C++), `PIL` (Python), `matplotlib` (Python)

## 🚀 How It Works (Polyglot Architecture)

This project uses Google Colab not just as a Python interpreter, but as a full virtualized Linux development server.

1. **Write (`%%writefile`):** A custom magic command is used to save a multi-line string directly as a native C++ source file (`fractal.cpp`) on the persistent filesystem.
2. **Compile (`!g++`):** A system-level Bash command triggers the `g++` compiler to build a production-optimized (`-O3`) binary (`render_engine`).
3. **Execute (`!./`):** A second Bash command executes the compiled C++ binary, performing millions of mathematical calculations to render the Mandelbrot fractal.
4. **Visualize (`Python`):** Python's extensive visualization libraries are deployed to read the raw image output and render it elegantly.

## 💻 Run it Yourself (Google Colab)

This project is optimized to run in any standard Google Colab or Jupyter Notebook environment.

1. Open the `.ipynb` notebook in Google Colab.
2. Run the first cell (`%%writefile`) to generate the C++ source file.
3. Run the second cell (`!g++`) to compile and execute the native binary.
4. Run the final cell to visualize the optimized C++ Mandelbrot output.
