# Ceramic Capacitor DC Bias Derating Analysis

This repository provides a Jupyter Notebook and supporting data for analyzing the DC bias derating behavior of ceramic capacitors. The analysis visualizes how real capacitance per area changes with applied DC bias for various MLCC packages, capacitance values, and dielectrics, using data exported from Murata's SimSurfing tool.

## Features

- Reads multiple CSV files containing DC bias derating curves for different capacitors.
- Normalizes capacitance by package area for fair comparison.
- Plots capacitance density vs. DC bias for all capacitors in the dataset.
- Highlights the capacitance at a user-defined target voltage (default: 3.3V).
- Annotates intersection points and provides summary statistics.

## Output Plots

Below are some plots generated by the notebook for different target voltages:

![Bias Derating at 3.3V](Images/Bias-Derating-at-3V3.avif)
*Bias Derating at 3.3V*

![Bias Derating at 5.0V](Images/Bias-Derating-at-5V0.avif)
*Bias Derating at 5.0V*

![Bias Derating at 12.0V](Images/Bias-Derating-at-12V0.avif)
*Bias Derating at 12.0V*

![Bias Derating at 24.0V](Images/Bias-Derating-at-24V0.avif)
*Bias Derating at 24.0V*

## Getting Started

### Prerequisites

- Python 3.10 or newer (tested with Python 3.13.3)
- Jupyter Notebook (or VS Code with Jupyter extension)

### Installation

1. Clone this repository:

   ```sh
   git clone https://github.com/your-username/Ceramic-Capacitor-Derating.git
   cd Ceramic-Capacitor-Derating
   ```

2. (Optional) Create and activate a virtual environment:

   ```sh
   python -m venv .venv
   # On Windows:
   .venv\Scripts\activate
   # On Linux/macOS:
   source .venv/bin/activate
   ```

3. Install required Python packages:

   ```sh
   pip install pandas==2.2.3 matplotlib==3.10.1
   ```

### Usage

1. Open `Bias-Voltage-Derating.ipynb` in Jupyter or VS Code.
2. Run all cells to generate the plots.
3. The notebook will process all CSV files in the `SimSurfing Bias Derating CSVs` folder.

### Data

- The `SimSurfing Bias Derating CSVs` folder contains example CSV files exported from Murata's SimSurfing tool.
- Each file should be named in the format: `Package, Capacitance, Voltage, Dielectric, Accuracy, csv` (e.g., `0603, 10uF, 10V, X5R, PM10.csv`).

### Output

- The notebook generates a plot showing capacitance per area vs. DC bias for all capacitors.
- A vertical line and markers indicate the capacitance at the target voltage.

## License

MIT License

## Acknowledgments

- Data generated using [Murata SimSurfing](https://ds.murata.co.jp/simsurfing/)
- Analysis and visualization by Chris Dirks 2025
