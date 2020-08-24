# Ubuntu-Anaconda-VSCode

Why Anaconda python? 
Easy for testing a few lines of python code.

1. setup ubuntu machine (VMWare Fusion), using ubuntu-20.04-desktop-amd64.iso
(step nr.5 will change your prompt, so I prefer to install anaconda in a dedicated vm.)

2. install git: 
# sudo apt install git

3. download anaconda installer from https://www.anaconda.com/distribution/
Anaconda3-2020.07-Linux-x86_64.sh
(source https://www.digitalocean.com/community/tutorials/how-to-install-anaconda-on-ubuntu-18-04-quickstart)

4. install anaconda:
# bash Anaconda3-2020.07-Linux-x86_64.sh
it will ask some questions, just say yes. 
Result is an installation in your home folder: ~/anaconda3/

5. start using anaconda bash:
# source ~/.bashrc
It will change your prompt into
(base) yourname@ubuntu:~$
So < (base) > is put in front of your prompt. I don't know how to undo this.

6. create anaconda enviromnent from base
- export conda from base into a file:
# (base) yourname@ubuntu:~$ conda list --explicit > Documents/Conda-spec-file.txt
- create new conda environment, testenv, from file:
# (base) yourname@ubuntu:~$ conda create --name testenv --file Documents/Conda-spec-file.txt

7. list conda environments:
(base) yourname@ubuntu:~$ conda info --envs
conda environments:

base                  *  /home/yourname/anaconda3
testenv                /home/yourname/anaconda3/envs/testenv

8. activate testenv environment:
# (base) yourname@ubuntu:~$ conda activate testenv
(testenv) yourname@ubuntu:~$

9. deactivate again: 
# (base) yourname@ubuntu:~$ conda deactivate


You can also create a conda environment with specific packages
See also:
https://docs.conda.io/projects/conda/en/latest/user-guide/



VSCode.
1. Use the Ubuntu Software installer, look for VSCode and install
2. Open VSCode and install Python Extension (from Microsoft, ms-python.python).
This extension is capable of running jupyter notebooks.
3. from the command palette, type
# Python: Create New Blank Jupyter Notebook
4. A new notebook appears, with a notebook menu. The notebook itself just like <Jupyter Lab>'s notebook. Pay attention to the menu on top op notebook file itself, you will need this to save the content and not VSCode menu 'File --> Save as'..



