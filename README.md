# Using Jupyter Notebooks

Install the jupyter notebook following the tutorial (here)[].

### Add Notebook Extensions

```conda install -c conda-forge jupyter_contrib_nbextensions```

Check the following:

* Collapsible Headings - Defaults

### Themify (Optional)

```pip install jupyterthemes```

I personally use a variant of the grade3 theme.

### Pretty Plots
Add the following lines towards the end of your ```~/.jupyter/custom/custom.css``` file.

```
.output {
    display: table-cell;
    text-align: center;
    vertical-align: middle;
}
```

This will make plots and figure outputs centred.

Additionaly, if you've used JupyterThemes, you can style the plots by calling ```jtplot_style()```, included with the startup script once at the top of your notebook.

### Startup Script
Place ```startup.py``` from this repository into your ```~/.ipython/profile_default/startup``` folder.

This will do all the necessary common setup including importing frequently used modules and setting up useful global variables and functions.

<hr>

# Installing MagNet

MagNet is a high-level library I'm developing on top of PyTorch that is aimed at making the creation, training, debugging and deployment of Deep Learning projects easy.

Clone the MagNet repository by running

```git clone https://github.com/svaisakh/magnet.git```

Hide the directory

```mv magnet .magnet```

Checkout the ```develop``` branch.

```git checkout develop```

Add the directory to the ```$PYTHONPATH``` variable by adding the following line to your ```.bashrc``` (Ubuntu) / ```.bash_profile``` (macOS)

```export PYTHONPATH=$PYTHONPATH:~/magnet```

Update by running

```source ~/.bashrc``` or ```source ~/.bash_profile``` as appropriate

<hr>

# Running Lesson Notebooks

Clone the appropriate repo

```git clone <repo_uri>```

where ```<repo_uri>``` can be found from the GitHub page of the lesson by clicking on the green _Clone or Download_ button.

Go into the repo

```cd <repo_name>```

Clone the conda environment that has all the needed packages and dependencies.

```conda env update```

If the environment name is <env_name>, activate it

```conda activate <env_name>```

Run the Jupyter Notebooks

```jupyter notebook```


