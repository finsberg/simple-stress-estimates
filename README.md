# Stress in simple geometries

Here we demonstrate how to compute stress in simple geometries such as an inflating cylinder.

We set up a racetrack cylinder geometry using the [`cardiac-geometriesx`](https://github.com/ComputationalPhysiology/cardiac-geometriesx) package, and then solve a static elasticity problem using the [`fenicsx-pulse`](https://github.com/finsberg/fenicsx-pulse) package.

## Running the code locally

First make sure to [install docker](https://docs.docker.com/get-docker/).

Then you can run the following command
```bash
docker run -e DISPLAY=":99.0" -e PYVISTA_JUPYTER_BACKEND="html" --rm -p 8888:8888  -w /home/shared -v $PWD:/home/shared -it ghcr.io/fenics/dolfinx/lab:v0.10.0 
```

This will start a jupyter lab server with FEniCSx installed, and display some information in the terminal, including a link to open jupyter lab in your browser, e.g
```
docker run --rm -p 8888:8888  -w /home/shared -v $PWD:/home/shared -it ghcr.io/fenics/dolfinx/lab:v0.10.0                                      
[I 2025-12-12 21:09:10.149 ServerApp] jupyter_lsp | extension was successfully linked.
[I 2025-12-12 21:09:10.149 ServerApp] jupyter_server_proxy | extension was successfully linked.
[I 2025-12-12 21:09:10.151 ServerApp] jupyter_server_terminals | extension was successfully linked.
[I 2025-12-12 21:09:10.153 ServerApp] jupyterlab | extension was successfully linked.
[I 2025-12-12 21:09:10.155 ServerApp] notebook | extension was successfully linked.
[I 2025-12-12 21:09:10.156 ServerApp] Writing Jupyter server cookie secret to /root/.local/share/jupyter/runtime/jupyter_cookie_secret
[I 2025-12-12 21:09:10.337 ServerApp] notebook_shim | extension was successfully linked.
[I 2025-12-12 21:09:10.346 ServerApp] notebook_shim | extension was successfully loaded.
[I 2025-12-12 21:09:10.347 ServerApp] jupyter_lsp | extension was successfully loaded.
[I 2025-12-12 21:09:10.353 ServerApp] jupyter_server_proxy | extension was successfully loaded.
[I 2025-12-12 21:09:10.354 ServerApp] jupyter_server_terminals | extension was successfully loaded.
[I 2025-12-12 21:09:10.355 LabApp] JupyterLab extension loaded from /dolfinx-env/lib/python3.12/site-packages/jupyterlab
[I 2025-12-12 21:09:10.355 LabApp] JupyterLab application directory is /dolfinx-env/share/jupyter/lab
[I 2025-12-12 21:09:10.355 LabApp] Extension Manager is 'pypi'.
[I 2025-12-12 21:09:10.392 ServerApp] jupyterlab | extension was successfully loaded.
[I 2025-12-12 21:09:10.394 ServerApp] notebook | extension was successfully loaded.
[I 2025-12-12 21:09:10.394 ServerApp] Serving notebooks from local directory: /home/shared
[I 2025-12-12 21:09:10.394 ServerApp] Jupyter Server 2.17.0 is running at:
[I 2025-12-12 21:09:10.394 ServerApp] http://1b772f431143:8888/lab?token=8d196cbcb8f9fdd61284cbdfba352b1ac71ccde2c9102578
[I 2025-12-12 21:09:10.394 ServerApp]     http://127.0.0.1:8888/lab?token=8d196cbcb8f9fdd61284cbdfba352b1ac71ccde2c9102578
```
The last line here is a link you can open in your browser to access jupyter lab, e.g http://127.0.0.1:8888/lab?token=8d196cbcb8f9fdd61284cbdfba352b1ac71ccde2c9102578
(NOTE: the token in your terminal will be different).

Once in jupyter lab, you should first run the notebook called `install.ipynb` to install the required python packages in the docker container.

Then you can run the e.g notebook `inflating_cylinder/normal_cylinder.ipynb` to set up and solve the inflating cylinder problem.

## LICENSE
MIT License 
