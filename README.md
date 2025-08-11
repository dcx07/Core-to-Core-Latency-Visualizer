# Core-to-Core Latency Visualizer

A tool to measure and visualize the latency between CPU cores on a system, helping developers and system administrators understand inter-core communication performance.

## Features

- Measures round-trip latency between pairs of CPU cores.
- Visualizes latency data using heatmaps or graphs.
- Supports configurable test durations and iterations.
- Outputs results in CSV and image formats.
- Cross-platform support (Linux, macOS, Windows).
- Easy-to-use command-line interface.

## Prerequisites

- C/C++ compiler (GCC, Clang, or MSVC).
- CMake (>=3.10).
- Python 3.6+ (for visualization scripts).
- matplotlib and seaborn Python libraries.

## Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/dcx07/Core-to-Core-Latency-Visualizer.git
   cd Core-to-Core-Latency-Visualizer
   ```

2. Build the project:
   ```bash
   mkdir build
   cd build
   cmake ..
   make
   ```

## Usage

Run the latency tester:
```bash
./core_latency_tester [options]
```

Common options:
- `-d, --duration <seconds>`: Duration of each test (default: 1.0).
- `-i, --iterations <number>`: Number of iterations per core pair (default: 1000).
- `-o, --output <path>`: Output CSV file (default: `latency_results.csv`).

Example:
```bash
./core_latency_tester -d 2.0 -i 500 -o results.csv
```

Visualize results:
```bash
python3 visualize_latency.py results.csv --output heatmap.png
```

## Contributing

Contributions are welcome! Please open issues or submit pull requests for bug fixes and new features.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.