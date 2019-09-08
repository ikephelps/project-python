# Excercise 00 - Git Setup
The contents of this project are managed using a [verson-control](https://en.wikipedia.org/wiki/Version_control) system called [Git](https://en.wikipedia.org/wiki/Git); by installing Git, changes to this (or any) project's [codebase](https://en.wikipedia.org/wiki/Codebase) can be tracked and shared without having to worry (too much) about who else might be attempting to alter the [repository](https://en.wikipedia.org/wiki/Repository_(version_control)) at the same time.

This excercise focuses on installing and configuring Git, and using it to clone (i.e. - download) this project to your local machine.

<blockquote>
<p>
    <cite>
        How am I reading this README if I haven't cloned the repository yet?!
    </cite>
</p>
<p>
    If you're a first-time Git user, odds are you're reading this at <i>GitHub</i>; if you've managed to clone this repository on your own, and you're confident in your Git configuration, feel free to skip this exercise.
</p>
</blockquote>

## 1. Installing `git`
Links to `git` [console application](https://en.wikipedia.org/wiki/Console_application) binaries can found here:

https://git-scm.com/downloads

Users interested in installing a Git [GUI](https://en.wikipedia.org/wiki/Graphical_user_interface) client should do so, *provided said client is bundled with the aforementioned `git` console application* - a GUI is a powerful tool, but **a)** `git` does everything Git-related, which isn't true of every GUI client, and **b)** the differences between the various GUIs would make this excercise impossible to document.

<details>
<summary>Recommended GUI Clients</summary> 
<ul>
    <li>
        <a href="https://desktop.github.com">GitHub Desktop</a> - requires *GitHub* account signup
    </li>
    <li>
        <a href="https://www.gitkraken.com/git-client">GitKraken</a> - requires *Axosoft* account signup; free for non-commercial development
    </li>
    <li>
        <a href="https://www.sourcetreeapp.com">SourceTree</a> - requires *Atlassian* account signup
    </li>
</ul>
</details>

Once you've downloaded and run your chosen `git` installer, open a [CLI](https://en.wikipedia.org/wiki/Command-line_interface) and execute the following command to verify the installation:
```bash
git --version
```
If you receive a response to the effect of "`git version 2.xx`", continue to the next step.

## 2. Git Setup
One small setup task, now that Git is installed; via CLI, enter:
```bash
git config --global --list
```
This command lists all of your current, global Git configuration (`.gitconfig`) variables, listed as key/value pairs; in this list, you may see the following keys:
- `user.name=Your Name`
- `user.email=your@email.here`

If they're set, and the values look correct, you're done with this step.  If you need to _add_ these key (or would like to change their values), enter the follwing commands in CLI:
```bash
git config --global user.name "Your Name"
git config --global user.email "your@email.here"
```
The `--global` flag in these commands sets their values globally, meaning they will be used for any `git` operations not specifically overridden in a local configuration (i.e. - `git config --local ...`); most immediatley, this information will appear in any commits you make to this or any other repository! 

## 3. Cloning this Repository
"Cloning" is the Git term for "copying an existing repository" - someone has already completed some work, and you're interested in leveraging that work in your own projects, in contributing some work of your own.

To clone *this* repository, navigate (via CLI) to the directory where this repository is to reside (on *your* computer; e.g. - `~/Documents/Projects`), and enter the following command:
```bash
git clone https://github.com/ikephelps/project-python.git
```
Once the little progress messages stop, you should see a new directory, "`project-python`", in your working directory. 

## 4. Configuring Remotes
<!-- reset orgin as upstream -->