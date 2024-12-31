# Final-Project-Network-Science

### Network Creation
Before you begin, follow this steps:

1. **Python 3.11**: Ensure you are using **Python 3.11** for compatibility with the dependencies.

2. **Install the required dependencies**:  
   You can install all necessary libraries using the `requirements_network_creation.txt` file. This can be done with the following command:

   ```bash
   pip install -r requirements_network_creation.txt

3. **Download the required data**:
   Make sure that you download the `gadm41_USA.gpkg` file from https://geodata.ucdavis.edu/gadm/gadm4.1/gpkg/gadm41_USA.gpkg 

- `Network_Creation.ipynb` retrieves the data at the county level, filters it for the states Georgia & South Carolina and creates a network by taking counties as nodes and common borders between counties as edges. This creates the following file `county_graph.gml`.

- `NTL_of_counties.ipynb` adds night time light time series as attributes to the network created by `Network_Creation.ipynb`. To run the code, ensure that `county_graph.gml` is in the working directory and download the night time light `.tif` files from our UZH Sharepoint Project Folder Number 14 `Night Time Light Data` folder into a working directory subfolder called `ntl_long_range`.

- `NX_NTL_weighted_edges.ipynb` adds the weights to the edges. It contains the function normalize weights, which takes a graph and a date as input and sums up the average NTL-values
for two neighbouring counties and divides them by two. Then it normalizes them between 0 & 1 and inverts the value, so that basic functions from the networkx pckg can be applied, such as 
betweenness_centrality for example, which will be used in the extended analysis.


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
