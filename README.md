## Get started guide

#### Clone this repository on your local computer

```
git clone https://github.com/glborres-biz/deep-learning-intro.git
```

#### Download and Install Anaconda Python 3.7

1. Go to https://www.anaconda.com/products/individual
2. Download the installer (Windows/MacOS/Linux)
3. Select Python 3.7 64-Bit Graphical Installer
4. Install the Anaconda
   - On _Advanced Options_, if you want the `conda` command available in other shell, check the **Add Anaconda to my PATH environment variable** (But this setup is not recommended because this can interfere with other software)
   - Instead, open Anaconda with the Start Menu and select **Anaconda Prompt**

#### Change to project folder

```
cd deep-learning-intro
```

#### Create the project environment

```
conda env create
```

Wait for the environment to be created.

#### Activate the environment (Mac/Linux/Windows)
```
conda activate deep-learning
```

Check that your prompt changed to

```
(deep-learning) $
```

#### Launch Jupyter Notebook

```
jupyter notebook
```

#### Open your browser to

```
http://localhost:8888
```

#### Run the Check environment Notebook

Go to the project folder, open the notebook `0_Check_Environment.ipynb` and run it. If you see the message:

    Houston we are go!

You are good to go! Enjoy!


#### Troubleshooting installation
If for some reason you don't see `Houston we are go!`, the simplest solution is to delete the environment and start from scratch again.

To remove the environment:

1. close the browser and go back to your terminal
2. stop jupyter notebook (CTRL-C)
3. deactivate the environment (Mac/Linux):

```
conda deactivate
```

4. deactivate the environment (Windows 10):

```
deactivate deep-learning
```

5. delete the environment:

```
conda remove -y -n deep-learning --all
```

6. restart from environment creation and make sure that each steps completes till the end.

#### Updating Conda

One thing you can also try is to update your conda executable. This may help if you already had Anaconda installed on your system.

```
conda update conda
```

These instructions have been tested on:

- Mac OSX Sierra 10.14.1
- Ubuntu 18.04
- Windows 10

## Running the project on Docker

Run this command from terminal in project directory and copy Jupyter notebook url to browser after installation.

```
docker-compose up
```

## Running the project on Google Colaboratory with free GPU support

Google offers a free platform to run Jupyter notebooks called Google Colaboratory. You need a Gmail or Google Apps email address to use it.

Follow these steps:

1. Open your browser and go to https://colab.research.google.com/
2. Choose the **GITHUB** tab and paste the repository address: `https://github.com/glborres-biz/deep-learning-intro.git` in the search bar.
3. Click on the notebook you would like to run
4. Enable GPU support in the `Edit -> Notebook Settings` menu
5. Enjoy running the notebook with GPU support!
6. If the notebook loads data from the repo you will have to download the data too. Follow these steps to do that:
   - Create a code cell at the top of the notebook
   - Clone the repository in Colab:
  ```
  !git clone https://github.com/glborres-biz/deep-learning-intro.git
  ```
   - Replace the `../data` path with `deep-learning-intro/data` in the cell that loads the data.
7. Enjoy!