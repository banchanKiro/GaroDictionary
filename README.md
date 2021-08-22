# Garo Dictionary

## Requirements
* python 3
* pip
* pipenv
* libpq-dev
* PostgreSQL
* PG Admin 4 (For easy postgres management)
## Installation
### Python 3
First ensure that `python 3` is installed. Run the command below to check.
```
python --version
```
Output:
```
Python 3.6.9
```
If this shows `Python 2.x.x`, try running:
```
python3 --version
```
If this does says that python3 is not found, then [install Python 3](https://phoenixnap.com/kb/how-to-install-python-3-ubuntu#ftoc-heading-1) by following the instructions on the link.
### pip
Next follow the instruction on [this link](https://linuxize.com/post/how-to-install-pip-on-ubuntu-18.04/#installing-pip-for-python-3) to install pip, a package manager for python.
### (Optional) Configuring BASH
If you have to access python by using `python3` in the terminal, you can set an alias to make it more convenient.

Open the bashrc file:
```
nano ~/.bashrc
```
Add the following lines (in order) to the file.
```
alias python=python3
alias pip='python -m pip'
alias pipenv='python -m pipenv'
```
Save the file. and run the following command to update bash.
```
source ~/.bashrc
```
The following steps shall be written assuming this step is done.

If not please replace `python` with `python3`, and `pip` with `python3 -m pip`.
### pipenv
Run the following command to install pipenv.
```
pip install --user pipenv
```
### libpq-dev
You need this packace in order to build psycopg2.

First make sure you have installed build-essentials package.
```
sudo apt update
sudo apt install build-essential
sudo apt-get install manpages-dev
```
Run
```
gcc --version
```
to confirm installation.

Next run the following command to install the package.
```
sudo apt update
sudo apt install libpq-dev
```
### PostgreSQL & PGAdmin4
To install and configure postgreSQL and PGadmin4, follow this [tutorial](https://stackoverflow.com/a/66489652).

After you finish the configuration, create a database and call it
```
garoDictionaryDB
```

Make sure to take note of the username and password of the user that you created. To avoid further changes, use `dbadmin` for the username and `admin` for the password and `garoDictionaryDB` for the database name.

If you are using a different username, password or database name change the lines in settings.py for the same.
### Installing Packages
In the root directory of the repository, run 
```
pipenv install
```
to install packages from the `PipFile`.

## Opening
Once all your installation is done, run 
```
pipenv shell
```
to open up the directory in a virtual environment. Then open the project in your code editor of choice.
```
code .
```
The above command is for VS Code.