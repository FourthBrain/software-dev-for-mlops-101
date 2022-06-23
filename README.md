<p align = "center" draggable=”false” ><img src="https://user-images.githubusercontent.com/37101144/161836199-fdb0219d-0361-4988-bf26-48b0fad160a3.png" 
     width="200px"
     height="auto"/>
</p>



## <h1 align="center" id="heading">:wave: Welcome to ML Software Developer 101!</h1>

Welcome to the beginning of your journey to becoming an ML Engineer (MLE)! :tada: Follow these steps to get your development environment teed up! After you've finished this set-up, feel free to go through the associated `Whodunit?`! 🕵️‍♀️


## :books: Quick Review
We will be using some terminal commands, so let's make sure you know what they are and what they do! 

| Command      | Stands For |  Description |
| ----------- | ----------- | -------------|
| `ls`      | long listing       | lists all files and directories in the present working directory |
| `ls -a`  | long listing all   |  lists hidden files as well |
| `cd {dirname}`      | change directory       | to change to a particular directory |
| `cd ~`   | change directory home        | navigate to HOME directory |
| `cd ..`      | change directory up       | move one level up |
| `cat {filename}`   | concatenate        | displays the file content |
| `sudo`      | superuser       | allows regular users to run programs with the security privileges of the superuser or root |
| `mv {filename} {newfilename}`   | move        | renames the file to new filename |
| `clear`      | clear       | clears the terminal screen |
| `mkdir {dirname}`   | make directory        | create new directory in present working directory or at specified path |
| `rm {filename}`   | remove        | remove file with given filename |
| `touch {filename}.{ext}`   | touch        | create new empty file |
| `rmdir {dirname}`   | remove directory        | deletes a directory |
| `ssh {username}@{ip-address} or {hostname}`   | secure shell        | login into a remote Linux machine using SSH |
| `CTRL + SHIFT + C` | copy | keyboard shortcut for copying from terminal |
| `CTRL + SHIFT + V` | paste | keyboard shortcut for pasting into terminal |

<p></p>

## :hammer_and_wrench: Tools We'll Be Using
We will also be using a few tools such as `git`, `conda`, and `pip`.
<details>
<summary>Git</summary>

Git is a free and open source distributed version control system designed to handle everything from small to very large projects. These are the commands we will be using with `git`:

`git clone` -> clone a remote repository to your local computer

`git add` -> add files to a commit

`git commit -m {message}` -> commit changes with a message

`git push` -> push commit to remote repository
</details>

<details>
<summary>Conda & Pip</summary>

Conda is an open-source, cross-platform, language-agnostic package manager and environment management system. We will use `pip` within `conda` environments to manage our package installations. `pip` is Python's package management system. `conda` comes with Anaconda. And Anaconda is a convenient way to set up your Python programming environment since it comes with an enviornment management tool (`conda`) and comes with extra packages that are commonly used in data science and ML.

Some commands we will use in this lesson when it comes to `conda` and `pip`:

`conda create --name mle-course python=3.8 pip` -> This creates a virtual environment. A virtual environment is a Python environment such that the Python interpreter, libraries, amnd scripts installed into it are isolated from those installed on other environments and any libraries installed on the system. So basically, this allows you to keep all your project's code/dependencies/libraries separated from other projects. You are specifically saying to create said environment with the name `mle-course`, use `python` version 3.8, and use `pip` as your package manager. The command `conda` invokes the underlying logic to actually make the virtual environment and manages said environments for you.

`conda activate mle-course` -> This activates the virtual environment you made with the above command for your current terminal session.

`pip install numpy pandas matplotlib` -> This installs the three packages mentioned - `numpy`, `pandas`, and `matplotlib`. `numpy` is used for scientific computing, `pandas` is used for data analysis, and `matplotlib` is used for data graphics. `pip` is the Python package manager and you are telling it to `install` the listed packages to your environment.
</details>

<details>
<summary>Jupyter Notebooks</summary>

Jupyter Notebooks are an incredibly useful tool for experimentation, iteration, exploration, and even production at some companies! 

They have the file extension `.ipynb` (IPYthon NoteBook)

You can learn more about Jupyter and their notebooks [here!](https://jupyter.org/)

In order to use a notebook, you'll first want to make sure you've installed `jupyter` in your environment

1. `conda activate <YOUR ENV NAME HERE>` 
2. `pip install jupyter`

From here, you can navigate to any folder containing a `.ipynb` file, and run the command `jupyter notebook`. This should launch a server, and provide you with a link. Navigate to the link in your browser in order to get started in your notebook! 

Be sure to terminate the server when you are done! Closing the webpage does not stop the server, so you'll need to make sure you do that manually in the terminal, or before you close the webpage with your server!

</details>

<p></p>

## :rocket: Let's Get Started! 
Let's start off by setting up our environment!  Review the environment setup instructions for the local environment that you'll be using in this course.
<details>
  <summary>Windows</summary>


* Install [Windows Subsystem for Linux](https://docs.microsoft.com/en-us/windows/wsl/install) using Powershell

```powershell
wsl --install -d Ubuntu-20.04
```
* Install [Windows Terminal](https://www.microsoft.com/en-us/p/windows-terminal/9n0dx20hk701?activetab=pivot:overviewtab) (You can even make it your [default!](https://devblogs.microsoft.com/commandline/windows-terminal-as-your-default-command-line-experience/))
* Install [Ubuntu](https://www.microsoft.com/en-us/p/ubuntu/9pdxgncfsczv?activetab=pivot:overviewtab)
    
(If you find yourself getting stuck on the WSL2 install, [here](https://www.youtube.com/watch?v=VMZH9Pj2dXw&ab_channel=StefanRows) is a link to video instructions)

Give it a test drive! 

![WindowsTerminal](https://user-images.githubusercontent.com/72572922/160048214-37f08855-8b29-4c13-9d25-e0f69806f752.jpg)

Continue by installing the following tools using [Windows Terminal](https://www.microsoft.com/en-us/p/windows-terminal/9n0dx20hk701?activetab=pivot:overviewtab) to setup your environment. When prompted, make sure to add `conda` to `init`.

| Tool | Purpose | Command                                                                                           |
| :-------- | :-------- | :------------------------------------------------------------------------------------------------ |
| :snake: **Anaconda**  | Python & ML Toolkits | `wget https://repo.anaconda.com/archive/Anaconda3-2021.11-Linux-x86_64.sh` <br> `bash Anaconda3-2021.11-Linux-x86_64.sh` <br> `source ~/.bashrc` |
| :octocat: **Git**  | Version Control | `sudo apt update && sudo apt upgrade` <br> `sudo apt install git-all`   |

</details>

<details>
  <summary>Linux (Debian/Ubuntu)</summary>

Open terminal using <kbd>Ctrl</kbd>+<kbd>Shift</kbd>+<kbd>T</kbd>. Enter the following commands in terminal to setup your environment. When prompted, make sure to add `conda` to `init`.
| Tool | Purpose | Command                                                                                           |
| :-------- | :-------- | :------------------------------------------------------------------------------------------------ |
| :snake: **Anaconda**  | Python & ML Toolkits | `wget https://repo.anaconda.com/archive/Anaconda3-2021.11-Linux-x86_64.sh` <br> `bash Anaconda3-2021.11-Linux-x86_64.sh` <br> `source ~/.bashrc` |
| :octocat: **Git**  | Version Control | `sudo apt update && sudo apt upgrade` <br> `sudo apt install git-all`   |

</details>

<details>
  <summary>macOS</summary>

To get started, we need to download the MacOS package manager, <strong>Homebrew</strong> :beer:, so that we can download the tools we'll be using in the course. If you don't already have Homebrew installed, run the following commands:

1. Open terminal using <kbd>⌘</kbd>+<kbd>Space</kbd> and type `terminal`.

2. Install Homebrew using the command below, following the command prompts:

    `/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"` 

3. Update Homebrew (This may take a few minutes)

    `git -C /usr/local/Homebrew/Library/Taps/homebrew/homebrew-core fetch --unshallow`

    `git -C /usr/local/Homebrew/Library/Taps/homebrew/homebrew-cask fetch`
     
4. Install the `wget` command to continue following along
     `brew install wget`

Enter the following commands in terminal to setup your environment. When prompted, make sure to add `conda` to `init`.

| Tool | Purpose | Command                                                                                           |
| :-------- | :-------- | :------------------------------------------------------------------------------------------------ |
| :snake: **Anaconda**  | Python & ML Toolkits | `wget https://repo.anaconda.com/archive/Anaconda3-2021.11-MacOSX-x86_64.sh` <br> `bash Anaconda3-2021.11-MacOSX-x86_64.sh` <br> `source ~/.bashrc` |
| :octocat: **Git**  | Version Control | `brew install git`   |

</details>

<p> </p>

## <img src="https://octodex.github.com/images/original.png" width=40px/> Let's Make Sure That GitHub is Ready to Roll!

If you don't already have one, make an account on [Github](https://github.com/)

<details>
  <summary>Github SSH Setup</summary>
  Secure Shell Protocol (SSH) provides a secure communication channel of an unsecured network.  Let's set it up!
  
  <p></p>

  1. Generate a Private/Public SSH Key Pair.
    
  ```console
  ssh-keygen -o -t rsa -C "your email address for github"
  ```

  2. Save file pair.  Default location `~/.ssh/id_rsa` is fine! 
  

  3. At the prompt, type in a secure passphrase.
  4. Copy the contents of the public key that we will share with GitHub. 

  
  * <strong>For WSL:</strong>

  ```console
  clip.exe < ~/.ssh/id_rsa.pub 
  ```

  * <strong>For MacOS:</strong>
  ```console
  pbcopy < ~/.ssh/id_rsa.pub 
  ```

  * <strong>For Linux:</strong>
  ```console
  xclip -sel c < ~/.ssh/id_rsa.pub 
  ```
  
  5. Go to your GitHub account and go to `Settings`. 
  
  6. Under `Access`, click on the `SSH and GPG keys` tabs on the left.

  ![Access Section](../img/github_access_section.png)

  7. Click on the `New SSH Key` button.
  
  ![New SSH Key](../img/github_new_ssh_key.png)
  
  8. Name the key, and paste the public key that you copied. Click the `Add SSH Key` button
  

  ![Add SSH Key](../img/github_add_ssh_key.png)

</details>

<details>
  <summary>Viewing the Repositories</summary>

Login and click on the top right user icon, then go to `repositories`. 

<p align="center">
  <img src="https://user-images.githubusercontent.com/37101144/162326947-3bfb4451-9854-41e8-9014-a02ed1322d66.png">
</p>
</details>


<details>
  <summary>Creating a New Repository</summary>

When viewing the respository page, click on `New` and proceed to create your repo.

<p align="center">
  <img src="https://user-images.githubusercontent.com/37101144/162327218-e1429ab2-2b24-4822-95bf-4411c2eb4a84.png">
</p>
<hr>

**Filling Respository Details**

Create the repository by inputting the following:
* `Repo name`
* `Repo description`
* Make repo `public`
* Add a `README`
* Add `.gitignore` (Python template)
* Add `license` (choose MIT)

Then click `Create Repository`.

<p align="center">
  <img src="https://user-images.githubusercontent.com/37101144/162327471-262a0931-c188-4976-8185-e70c4d108f71.png">
</p>

</details>

<details>

<summary>Clone Your Repo</summary>

  1. Open your terminal and navigate to a place where you would like to make a directory to hold all your files for this class using the command `cd`. 


  ```console
  cd {directory name}
  ```
  
  2. Once there, make a top level directory using `mkdir`. 

  ```console
  mkdir {directory name}
  ```

  3. `cd` into it and make another directory called `code`. 

  ```console
  cd {directory name}
  ```

  ```console
  mkdir code
  ```

  4. `cd` into it and run your `git clone {your repo url}` command. 

  ```console
  cd code
  ```

  ```console
  git clone {your repo url}
  ```
     
  5. Now let's get into our directory so we can access the contents of the repo!

  ```console
  cd {your repo name}
  ```
     
</details>

<details>
  <summary>Adding The FourthBrain Whodunit? Content to Your Repo</summary>

  1. Check your remote git. 

  ```console
  git remote -v
  ```

  At this point, you should just have access to your own repo with an origin branch with both fetch and push options.

  2. Let's setup our global configuration:

  ```console
  git config --global user.email "your email address"
  ```

  ```console
  git config --global user.name "your name"
  ```

  3. Let's add a local branch for development.

  ```console
  git checkout -b LocalDev
  ```

  You can change anything here in this branch!

  ```console
  git add .
  ```

  Commit the changes with the branch addition.

  ```console
  git commit -m "Adding a LocalDev branch."
  ```

  4. Let's push our local changes to our remote repo.

  ```console
  git checkout main
  ```

  ```console
  git merge LocalDev
  ```

  ```console
  git push origin main
  ```


5. Add the Whodunit (WD) repo as an extra remote repo:

  ```console
  git remote add WD git@github.com:FourthBrain/whodunit.git
  ```

  Let's check our remote repos:

  ```console
  git remote -v
  ```

  At this point, you should have access to both your own repo and FourthBrain and should see something like this:

  ```console
  WD    git@github.com:FourthBrain/whodunit.git (fetch)
  WD    git@github.com:FourthBrain/whodunit.git (push)
  origin git@github.com:rafatisina/TestRepo.git (fetch)
  origin git@github.com:rafatisina/TestRepo.git (push)
  ```

  Let's update our local repos:

  ```console
  git fetch --all
  ```

  Make a new branch for the Whodunit material (WDBranch).
  ```console
  git checkout --track -b WDBranch WD/main
  ```
  
  You should see something like this:
  
  ```console
  Branch 'WDBranch' set up to track remote branch 'main' from 'WD'.
  ```

  You can visually check whether you are in that branch:

  ```console
  git log --all --graph
  ```

  Now let's push our updated local repo to our remote repo!

  ```console
  git checkout main
  ```

  ```console
  git merge WDBranch --allow-unrelated-histories
  ```

  If there are any conflicts you'll need to resolve them.
  ```console
  git add .
  ```
  
  ```console
  git commit -m "message-here"
  ```
  
  ```console
  git push origin main
  ```

  From now on... after each release follow these steps to update your repo with new content:
  ```console
  git fetch --all
  git checkout WDBranch
  git merge --ff-only @{u}
  git add .
  git commit -m "branch is updated"
  git checkout main
  git merge WDBranch --allow-unrelated-histories
  ```

  You will be asked to add a comment about why this change is necessary --> add a message.
  
  ```console
  git push origin main
  ```
</details>


<p> </p>

## <img src="https://jupyter.org/assets/homepage/main-logo.svg" width=40px/> Bringing it all together with Jupyter notebooks!
<details>
<summary>Jupyter notebooks</summary>

  1. First, make sure that you are in your repo's main directory.  Then navigate to the MLE-8 folder of your repo.  `HINT:` You can use `pwd` to see the directory you're currently in.

  2. Navigate to the `notebooks` folder within the `software-dev-for-ml-101` folder.

  ```console
  cd software-dev-for-ml-101/notebooks
  ```

  3. Activate your conda environment that you created above.
  
  ```console
  conda activate <YOUR ENV NAME HERE>
  ```

  4. Run the `jupyter notebook` command. 

  5. A new window should open in your browser with the Jupyter Server.  If not copy and paste the give link in your browser.

  6. Open the `unix-conda-pip.ipynb` notebook and go through the demo.
     
  Note: JupyterLab is an acceptable alternative to Jupyter Notebooks if you prefer JupyterLab!

</details>

<p></p>

# :detective: Whodunit? 
Now let's practice  what you have learned by playing the [Whodunit?](https://github.com/FourthBrain/whodunit) game!

### That's it for now!  And so it begins.... :)
