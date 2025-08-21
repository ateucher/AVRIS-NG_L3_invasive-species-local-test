# Testing local execution of Notebooks access NASA Earthdata in AWS US West 2

This is a test of running a notebook locally that accesses NASA Earthdata in
AWS US West 2. This notebook has previously been run successfully in the NASA-Openscapes
JupyterHub as part of a workshop at [ESA 2025](https://ornldaac.github.io/airborne/notebooks/AVIRIS-NG_L3_invasive_species.html).

## Running the Notebook

I used `uv` to set up the project and create a virtual environment (`.venv`). 

The dependencies are listed in the `pyproject.toml` file. You can install them and 
set up the environemt with:

```bash
uv lock
uv sync
```

Then the notebook can be run.

Note: the files `ct_invasive.gpkg` and `dsp.nc` are not included in the repository; they 
were downloaded from the Hub for local use.

### Observations

The notebook runs successfully and produces the expected output. The cell that
extracts the spectra from each land plot runs more slowly than in the JupyterHub 
(about 3 minutes compared to 1 minute in the Hub), but it does run 
successfully.

Reprojecting the test data to create the final plot takes a very long time (about 20 minutes), though
this actually crashed repeatedly in the JupyterHub.
