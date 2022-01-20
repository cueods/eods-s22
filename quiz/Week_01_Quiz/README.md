# EODS-S22 Week 1 Quiz

Note: Below, the `$` indicates the command line. You don't need to enter this character. Your terminal prompt may end in something else, like a '>'.

## Part 1: Install git and Clone the Course Repo

1. If you don't already have git installed, download and install git from https://git-scm.com/downloads

2. Open a command line terminal:
    - Windows: Start -> Git Bash
    - MacOS: Command+Space -> "Terminal"
    - Linux: Terminal

3.   Navigate to a folder where you keep your projects. Example:

        $ cd /c/proj/

4.  Clone the course repo from https://github.com/cueods/eods-s22

        $ git clone https://github.com/cueods/eods-s22.git

---


## Part 2: Install Anaconda Python, Create the course Environment and Create a Jupyter Notebook

1. Download and install Anaconda 3 Individual Edition from https://www.anaconda.com/products/individual

    - Windows: 64-Bit Graphical Installer
    - MacOS: (recommended) 64-Bit Command Line Installer
    - Linux: 64-Bit (x86) Installer

    Follow the instructions here for your os: https://docs.anaconda.com/anaconda/install/
    (recommended) “Do you wish the installer to initialize Anaconda3 by running conda init?” : “yes”. 

2. Open a new command line terminal
    - Windows: Start -> Anaconda Prompt (Anaconda3)
    - MacOS: Command+Space -> "Terminal"
    - Linux: Terminal

3. Navigate to where you cloned the course repo
    
        (base) $ cd ~/proj/eods-s22

4. If you are in the base anaconda environment, you should see `(base)` in the shell prompt (see example above).
If you don't see `(base)`, activate the base environment with:
    
        $ conda activate
    
5. Create a new virtual environment using the requirements file:

        (base) $ conda env create -f docs/requirements.yml

6. Activate the new environment

        (base) $ conda activate eods-s22

7. Add the new environment to jupyter

        (eods-s22) $ python -m ipykernel install --user --name eods-s22
        
8. Jupyter Notebook server (assuming you are going to use eods-s22 environment)

        (eods-s22) $ jupyter notebook
		
	In case you prefer to use (base) environment, return to the base environment and launch Jupyter Notebook server:
	
        (eods-s22) $ conda deactivate
        (base) $ jupyter notebook
	
	(if you are using base environment, then in step 10, instead of using newly created kernel, you can use New -> Python 3 intead.)

9. In Jupyter, navigate to the folder: quiz/week_01_quiz

10. Open a new notebook using the newly created kernel: New -> eods-s22 (or New -> Python 3) 

11. Rename the notebook "week_01_quiz-uni", replacing uni with your unique CUID

12. In the first cell, copy the following code and run:

        import sys
        import pandas
        import sklearn
        print('python version:',sys.version)
        print('pandas version:',pandas.__version__)
        print('sklearn version:',sklearn.__version__)
        print('pandas path:',pandas.__path__)
		
13. Click the link in the 2nd Cell, and fill in the survey

14. After that, create the 3rd Cell, and write code to print 

    I have DONE the survey for EODS, my UNI is: {your UNI}, and my github id is:{your githubID} 
    
    (Please note that this helps us link your UNI with your githubID so grades can be assigned)

---

## Part 3: Submission

1. Click the link that I shared on Canvas to get your local repository of the quiz

2. In your github account, https://github.com/cueodsml/Week_01_Quiz-UNI-{YourGithubID}

3. Choose uploade files, then click "Drag files here to add them to your repository Or choose your files"

Choose the file that you created in Part 2 above, i.e., "Week_01_Quiz-UNI" (UNI is your uniqe CUID)

4. Add an optional extended description

5. Click "Commit changes"
-- this essentially have submitted your quiz (you can repeat 1-4 before due date in case you need to make any change to your code)

