React Native JavaScript Combiner
================================

This repository contains a Python script designed to combine all JavaScript files from a React Native project into a single file. This script is particularly useful for simplifying the review and analysis of large codebases by merging all relevant source code into one comprehensive file, excluding non-essential directories and files typically found in a development environment.

Features
--------

*   **Directory Exclusion**: Automatically excludes common non-source directories such as `node_modules`, `.git`, `build`, `dist`, `ios`, `android`, `__tests__`, and `coverage`.
*   **File Exclusion**: Skips over configuration and miscellaneous files that do not contribute to the application's core functionality, like `.babelrc`, `.eslintrc.js`, `.prettierrc`, `webpack.config.js`, `.env`, and `babel.config.js`.
*   **Progress Tracking**: Utilizes `tqdm` to display a progress bar, providing visual feedback during the file combining process.

Prerequisites
-------------

Before running the script, ensure you have the following installed:

*   Python 3
*   `tqdm` library

You can install `tqdm` using pip:


`pip install tqdm`

Usage
-----

To use the script, simply specify the directory of your React Native project and the desired output file name for the combined JavaScript file. Modify the script's parameters accordingly and run it in a Python environment capable of executing Jupyter Notebooks or regular Python scripts.

Example command:


`combine_js_files_react_native_with_progress('path/to/your/react_native_project', 'combined_output.js')`

Replace `'path/to/your/react_native_project'` with the actual path to your project directory and `'combined_output.js'` with your chosen output filename.

How It Works
------------

The script walks through the specified project directory, gathering all `.js` files while skipping the directories and files specified in the exclusion lists. Each JavaScript file's contents are read and combined into a single output file, with each section prefaced by a comment indicating the original file path to maintain traceability.

Contributions
-------------

Contributions to this project are welcome. Please ensure that any pull requests or issues adhere to the existing coding style and functionality scope.

