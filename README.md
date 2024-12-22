# Final-Project-Network-Science

- `NTL_of_counties.ipynb` adds night time light time series as attributes to the network created by `Network_Creation.ipynb`. To run the code, ensure that `county_graph.gml` is in the working directory and download the night time light `.tif` files from our project folder number 14 (https://uzh.sharepoint.com/:f:/s/NetworkScienceHS24/EhnFsb0ubr9AqxtA4KFpKIoB73CMLJClc0SzJp8Z1c9uag?e=v0PniN) into a subfolder called `ntl_long_range`.


### Network Analysis


### Extended Analysis
For the extended analysis the previously generated `county_graph_with_ntl.gml` file was used. All relevant code can be found in the Jupyter Notebook `Extended_Analysis.ipynb`. To run the code, please follow these instructions: 
  - Open the terminal, navigate to `Extended_Analysis.ipynb` and create a virtual environment: `$ python3 -m venv myenv`
  - Activate the virtual environment: `$ source myenv/bin/activate`
  - Install the requirements through: `$ pip3 install -r requirements_extended_analysis.txt`
  - Add venv as a kernel to VS Code: `$ python3 -m ipykernel install --user --name=venv --display-name "Python (myenv)"`
  - Run code.
