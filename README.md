# Final-Project-Network-Science

- `NTL_of_counties.ipynb` adds night time light time series as attributes to the network created by `Network_Creation.ipynb`. To run the code, ensure that `county_graph.gml` is in the working directory and download the night time light `.tif` files from our project folder number 14 (https://uzh.sharepoint.com/:f:/s/NetworkScienceHS24/EhnFsb0ubr9AqxtA4KFpKIoB73CMLJClc0SzJp8Z1c9uag?e=v0PniN) into a subfolder called `ntl_long_range`.


### Network Analysis
This repository contains a network analysis project that requires the `county_graph_with_ntl.gml` file to function properly. Follow the instructions below to set up and run the analysis.

#### Prerequisites

Before you begin, ensure you have the following:

1. **Python 3.11**: Ensure you are using **Python 3.11** for compatibility with the dependencies.

2. **The `county_graph_with_ntl.gml` file**: This file is required for the analysis. It should be in the same directory as the `analysis.ipynb` notebook file.  
   - If the `.gml` file is not in the same directory, you will need to update the file path in the code. Locate the path where the `.gml` file is stored and modify the path in the code accordingly.

3. **Install the required dependencies**:  
   You can install all necessary libraries using the `requirements_analysis.txt` file. This can be done with the following command:

   ```bash
   pip install -r requirements_analysis.txt

Once the requirements are installed, you can run the cells in the notebook to perform the network analysis.

### Heatmap Analysis
This guide will help you prepare and run the heatmap analysis efficiently. Follow these steps to ensure that all prerequisites are met and the analysis runs smoothly. The heatmap analysis uses network data to generate insightful visualizations and requires a specific setup before you can execute the `heatmaps.ipynb` notebook.

#### Prerequisites

1. **Python 3.11**  
   Ensure you are using **Python 3.11** for compatibility with the dependencies.

2. **The `county_graph_with_ntl.gml` file**  
   This file is required for the analysis and should be in the same directory as the `heatmaps.ipynb` notebook file.  
   - If the `.gml` file is not in the same directory, you will need to update the file path in the code. Locate the path where the `.gml` file is stored and modify the path in the code accordingly.

3. **Install the required dependencies**  
   You can install all necessary libraries using the `requirements_heatmap.txt` file. Run the following command in your terminal:

   ```bash
   pip install -r requirements_heatmap.txt
   
Once the prerequisites are met, open the heatmaps.ipynb notebook and run the cells to perform the network analysis.

### Extended Analysis
For the extended analysis the previously generated `county_graph_with_ntl.gml` file was used. All relevant code can be found in the Jupyter Notebook `Extended_Analysis.ipynb`. To run the code, please follow these instructions: 
  - Open the terminal, navigate to `Extended_Analysis.ipynb` and create a virtual environment: `$ python3 -m venv myenv`
  - Activate the virtual environment: `$ source myenv/bin/activate`
  - Install the requirements through: `$ pip3 install -r requirements_extended_analysis.txt`
  - Add venv as a kernel to VS Code: `$ python3 -m ipykernel install --user --name=venv --display-name "Python (myenv)"`
  - Run code.
