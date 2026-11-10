# Dask Parallel Processing

A hands-on Jupyter notebook demonstrating how to build and execute parallel task graphs with Dask. The activity compares sequential and parallel execution, measures runtime, and visualizes task dependencies.

## What You'll Learn

- Define work with Dask's `delayed` function.
- Build a task graph from dependent and independent operations.
- Execute a graph and compare its runtime with a sequential implementation.
- Visualize task dependencies.
- Understand why parallel processing can help with larger workloads.

## Repository Contents

- [`dask_parallel_processing.ipynb`](./dask_parallel_processing.ipynb) — the completed, executable activity notebook.

## Requirements

- Python 3.9 or later
- Jupyter Notebook or JupyterLab
- Dask and the Python Graphviz package
- The Graphviz system executable (`dot`) to render task-graph visualizations

Install the Python dependencies in the environment used by your Jupyter kernel:

```bash
python -m pip install jupyter dask graphviz
```

On macOS, install the Graphviz system executable with Homebrew:

```bash
brew install graphviz
dot -V
```

If `dot -V` reports a version, Graphviz is available on your `PATH`. Restart VS Code or Jupyter after installing Graphviz so the notebook kernel can see the updated environment.

## Run the Notebook

Clone the repository and change into its directory:

```bash
git clone https://github.com/GHshail/dask-parallel-processing.git
cd dask-parallel-processing
```

Start Jupyter:

```bash
jupyter notebook
```

Open `dask_parallel_processing.ipynb`, select the Python environment where the dependencies are installed, and run all cells from top to bottom. The examples include one-second sleeps to simulate longer-running work; measured runtimes vary by machine and scheduler overhead.

## Expected Result

The notebook demonstrates that independent delayed tasks can run concurrently and form a Dask task graph. In the final example, the calculated sum is `90`. Actual runtime improvements depend on the workload, available hardware, and the overhead of scheduling tasks.
