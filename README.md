# RStuidoJupyterNotebook
How to use R in Jupyter Notebook and How to use Python in RStudio

**Yes, I know we should use R in RStudio and Python in Jupyter Notebook. But just for FUN!**

## How to use R in Jupyter Notebook

Assume you have already installed anaconda environment and jupyter notebook in your computer. If not, go to [https://www.anaconda.com/download/] or google how to install anaconda and jupyter notebook. The following guide is made in Windows 10, it might be different for other systems.


Step 1: Open an anaconda prompt https://github.com/Inhenn/RStuidoJupyterNotebook/blob/master/10.png

<img src=https://github.com/Inhenn/RStuidoJupyterNotebook/blob/master/18.png height="600" width="400">

Step 2: In the directory you desired, type "conda install -c r r-irkernel" to install irkernel.
(Referring to [https://irkernel.github.io/] )

<img src=https://github.com/Inhenn/RStuidoJupyterNotebook/blob/master/3.png height="300" width="600" >

<img src=https://github.com/Inhenn/RStuidoJupyterNotebook/blob/master/4.png  height="300" width="600" >

Yes Yes Yes!!!

Kernel Installed

<img src=https://github.com/Inhenn/RStuidoJupyterNotebook/blob/master/5.png  height="300" width="600" >

Step 4: If you launch jupyter notebook, you will see a new kernel called r

<img src=https://github.com/Inhenn/RStuidoJupyterNotebook/blob/master/6.png  height="300" width="600" >

Step 5: Now, we need to go back and install some packages. In anaconda prompt, type "r" to launch R, and type "install.packages(" packages you want to install ")", select a CRAN mirror. (Referring to [https://irkernel.github.io/installation/])

<img src=https://github.com/Inhenn/RStuidoJupyterNotebook/blob/master/20.png  height="400" width="600" >

Step 6: Now launch jupyter notebook again, and open a new file in "r", we get our first Notebook in R

<img src=https://github.com/Inhenn/RStuidoJupyterNotebook/blob/master/13.png  height="300" width="600" >

<img src=https://github.com/Inhenn/RStuidoJupyterNotebook/blob/master/14.png  height="400" width="600" >


## How to use Python in Rstudio

Assume you have also installed R and Rstudio in your computer, if not go to download R and Rstudio [https://www.rstudio.com/products/rstudio/download/]. Also you need to have anaconda and python in your computer.

Step 1:Launch Rstudio, open a new script, install the package "reticulate"

Step 2: Type

library(reticulate)\
use_condaenv("C:/Software/PythonAnaconda/envs")\
#use_python("/usr/local/bin/python")\
#use_virtualenv("~/myenv")\
py_config()\
print("hello world")


Use the library, specify the python path or conda environment or virtual env. Here I use my condaenv as an example. If you do not know where is your python or conda environment, open a jupyter notebook and type 


import os\
import sys\
os.path.dirname(sys.executable)


Then, do py_config in Rstudio, and we are in the python environment!!!

<img src=https://github.com/Inhenn/RStuidoJupyterNotebook/blob/master/22.png  height="400" width="600" >

We can also run python in a markdown environment, by doing the same thing. Initialize python in the first chunk. In the second chunk, we can directly use 


 ` ```{python}

 ` ```

and write python code. The nice thing about markdown file is that we have colors in variable names and functions just like a normal python editor. (Refering to [https://cran.r-project.org/web/packages/reticulate/vignettes/r_markdown.html])

<img src=https://github.com/Inhenn/RStuidoJupyterNotebook/blob/master/17.png  height="400" width="600" >






