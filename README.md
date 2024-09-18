# DataFrame Viewer

A Python module to display large pandas DataFrames with auto-adjusted column widths in a web browser.

## Overview

This module allows you to visualize pandas DataFrames in a more readable format by rendering them as HTML tables in your default web browser. It includes basic styling to ensure that column widths are auto-adjusted, making it easier to view large DataFrames without saving them to disk.

## Features

- **Auto-Adjusted Column Widths**: Improves readability by adjusting column widths dynamically.
- **HTML Rendering**: Displays DataFrames in a formatted HTML table.
- **No Disk Writes**: Uses temporary files that are automatically deleted after use.

## Installation

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/TheKola/df-viewer.git
2. **Navigate to the Project Directory**:
    ```bash
    cd dataframe-viewer
3. **Install dependendencies**:
    ```bash
    pip install -r requirnments.text

## Usage

1. Import the Module:
    ```bash
    from df_viewer import view_df
2. Create a DataFrame and view it:
    ```bash
    import pandas as pd
    from df_viewer import view_dataframe

    # Example DataFrame
    data = {
    'Name': ['Alice', 'Bob', 'Charlie'],
    'Occupation': ['Engineer', 'Doctor', 'Artist'],
    'Location': ['New York', 'Los Angeles', 'Chicago']
    }
    df = pd.DataFrame(data)

    # View the DataFrame in a web browser
    view_df(df)

## Output
<picture>
    <style>
    table {
        width: 100%;
        border-collapse: collapse;
    }
    th, td {
        padding: 8px;
        text-align: left;
        white-space: nowrap;
    }
    th {
        background-color: #f2f2f2;
    }
    </style>
    <table border="1" class="dataframe" >
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Name</th>
      <th>Occupation</th>
      <th>Location</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>Alice</td>
      <td>Engineer</td>
      <td>New York</td>
    </tr>
    <tr>
      <th>1</th>
      <td>Bob</td>
      <td>Doctor</td>
      <td>Los Angeles</td>
    </tr>
    <tr>
      <th>2</th>
      <td>Charlie</td>
      <td>Artist</td>
      <td>Chicago</td>
    </tr>
  </tbody>
</table>
</picture>

## Contributing
Contributions are welcome! Please read the [contributing guidelines](CONTRIBUTING.md) for more details.

## License
This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
