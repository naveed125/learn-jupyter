# Learn Jupyter

Follow the following steps to create a local jupyter environment using `Conda`

1. Install anaconda first
2. Run `conda env list` This should just list one evironment called base.
3. On windows, start Anaconda command prompt as admin and cd into your project directory. Then setup the env using conda

```
conda create --yes --name learnjupyter
conda activate learnjupyter
```

4.1 Now that you are in the `learnjupyter` env, install jupyter labs by running the following commands. I prefer this over user Jupyter Notebook

```
conda install -y -c conda-forge jupyterlab
conda install -y -c conda-forge nb_conda_kernels
conda install pip
pip install jupyter
pip install matplotlib 
pip install astropy
```

4.2 Install using pip

```commandline
python -m venv venv
.\venv\Scripts\activate
pip install jupyterlab
```

5. Start Jupyter

```
juypter lab
-- OR--
jupter notebook
```

This will start a local web server at:

http://localhost:8888/tree?token=sfsdfsdfsdfsfsaf

Look for the URL printed on the command line.

6. Continue in browser and create a new notebook. Everytime a new notebook is created a *.ipynb file is created for it in the local directoy. 
Try some of the example from [this](https://realpython.com/jupyter-notebook-introduction/) tutorial.



