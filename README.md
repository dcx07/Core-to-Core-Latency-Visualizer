# C2C Latency Visualizer

This is a simple, single-page HTML tool for visualizing core-to-core (C2C) latency data. It takes a comma-separated matrix of latency values and generates a color-coded heatmap, making it easy to understand the latency characteristics between different CPU cores.

## Features

-   **Interactive Heatmap:** Generates a clear and easy-to-read heatmap from your data.
-   **Simple Data Input:** Just copy and paste your comma-separated data.
-   **Color-Coded Visualization:** Latency values are represented by a color gradient from blue (low latency) to red (high latency) for quick analysis.
-   **Handles Missing Data:** Correctly processes cells with non-numeric values (e.g., 'x') by marking them as invalid.
-   **Dynamic Legend:** A legend is generated based on the minimum and maximum latency values in your data.
-   **No Server Needed:** Runs entirely in your web browser. No installation required.

## How to Use

1.  **Open the File:** Open the `c2c.html` file in any modern web browser (like Chrome, Firefox, or Edge).
2.  **Paste Your Data:** Copy your C2C latency data and paste it into the text area. The data should be in a comma-separated matrix format. Each row represents a source core, and each column represents a target core. Use 'x' or any non-numeric character for unavailable or invalid latency measurements.

    **Example Data Format:**
    ```
    0, 10.5, 15.2, 20.1
    10.4, 0, 21.0, 16.3
    15.1, 20.9, 0, 12.5
    20.0, 16.2, 12.4, 0
    ```

3.  **Visualize:** Click the "Visualize" button.
4.  **Analyze:** A heatmap will be generated below the button, showing the latency between each pair of cores. Hover over the cells to see the exact values. The color legend at the bottom indicates the scale of latency values (in nanoseconds).
