### Let's start with simple words that everyone understands,What is Git? :computer:

![Alt Text](https://media.giphy.com/media/VGbx7xfluiGnY4KwBF/giphy.gif)

- Is it a programming language? - :negative_squared_cross_mark:
- Is it a database? - :negative_squared_cross_mark:
- Is it an operating system? - :negative_squared_cross_mark:
- I was wondering what is git doing? So what is Git? What exactly is his job?

To understand what it is, we must first understand the problem that led to its existence, take this as a simple example, to get it.

### The problem :confused:

You are working on a big project as programmer, and you works on it for along time, and you really made progress, during working on it, suddenly found your self with trouble, you wrote function that made a messy in your code, and you wish that you can undo or knowing where exactly the project work successfully. So you think you are smart enough to not fall in this problem again.

![Alt Text](https://media.giphy.com/media/l2R024uE283zkmdfW/giphy.gif)

You starts create a folder for your project, and give it a name, date and time.
And you will make an another copy, every time you add new feature. And this will help you to find any copy you want.

![](https://i.imgur.com/gpXIREQ.png)

After a while, the project became bigger, and sometimes you forget to create a new folder and after all it will be many folders and you will not know which one is working perfect and has the specific feature that you want.
You will waste time and effort to know which one.

![Alt Text](https://media.giphy.com/media/108KUzjTMEp2gw/giphy.gif)

### So, the soultion is

version control system

## What is version control system (VCS)?

Version control, also known as revision control or source control, is the management of changes to documents, computer programs, large websites, and other collections of information. Each revision is associated with a timestamp and the person making the change. Revisions can be compared, restored, and with some types of files, merged.[1]

Version control systems (VCS) most commonly run as stand-alone applications, but may also be embedded in various types of software, including integrated development environments (IDEs).

### Discussion

Version control implements a systematic approach to recording and managing changes in files. At its simplest, version control involves taking ‘snapshots’ of your file at different stages. This snapshot records information about when the snapshot was made, and also about what changes occurred between different snapshots. This allows you to ‘rewind’ your file to an older version. From this basic aim of version control, a range of other possibilities is made available.

#### Version control allows you to:

- Track developments and changes in your files
- Record the changes you made to your file in a way that you will be able to understand later
- Experiment with different versions of a file while maintaining the original version
- ‘Merge’ two versions of a file and manage conflicts between versions
- Revert changes, moving ‘backward’ through your history to previous versions of your file.

Version control is particularly useful for facilitating collaboration. One of the original motivations behind version control systems was to allow different people to work on large projects together. Using version control to collaborate allows for a greater deal of flexibility and control than many other solutions. As an example, it would be possible for two people to work on a file at the same time and then merge these together. If there were ‘conflicts’ between the two versions, the version control system would allow you to see these conflicts and make an active decision about how to ‘merge’ these different versions into a new ‘third’ document. With this approach you would also retain a ‘history’ of the previous version should you wish to revert back to one of these later on.

Popular version control systems include:

- Git
- Helix VCS
- Microsoft Team Foundation Server
- Subversion

### The following focuses on using the Git version control system.

#### what is Git?

Git is a Version Control System for tracking changes in computer files.

- **Distributed version control** (**decentralized**): Many developers can work on the single project without having to be on the same network.
- **Coordinate work between multiple developers**:
- **Who made what changes and when**
- **Revert back at any time**
- **Local and remote repositories**
  **What is repository?**
  We have two types of repos; local which is on our computer and remote which is hosted on somebody's else server or computer.
  The purpose of a remote repository (eg, **GitHub**) is to publish your code to the world or to some people and allow them to read or write it, so if you are the only developer, you don't really need a remote/central repo.

## Initializing a git local repository

#### Local implementation of using git and version control

inside your **terminal**, follow the next commands:

```
cd Desktop
mkdir FOLDER_NAME
cd FOLDER_NAME
ls
touch file1.txt <!--then add some text-->
git init
ls -a <!-- .git is used to track and commit your changes and to perform version control-->
git status
git add file1.txt
git status
git commit -m "complete my first file"
git log
touch file2.txt file3.txt <!--then add some text-->
git status
git add .
git status
git commit -m "complete my second and third files"
git log
```

![drawing](https://i.stack.imgur.com/UvZ0M.png)

## What is GitHub?

#### the largest host of source code in the world

The world's leading software development platform.
GitHub brings together the world's largest community of developers to discover, share, and build better software. From open source projects to private projects.

### Open Source

Open source refers to any program whose source code is made available for use or modification as users or other developers see fit. Open source software is usually developed as a public collaboration and made freely available.

## How to create a remote repository?

1. create a **repository**
2. clone the repo you've created git
3. move into the newly created directory
4. raise your **issues** on the work to be done
5. create a new **branch** with a unique and descriptive name
6. leave the **master** branch by switching to the new branch you have just created
7. write your code
8. add the new files to the **staging** area
9. commit your changes
10. push your local version up to GitHub
11. create a **pull r**equest
12. wait it to be **merged**

## Git & GitHub terminology

### Working Directory

It is the folder/directory where we initialize our git repository by using the command

```
git init
```

### Staging Area

It is an intermediate place between Working Directory and Local Repository to figure out what the things you want git to ignore and what the things you want it to be tracked.

### Repository

A repository is like a folder for your project. Your project's repository contains all of your project's files and stores each file's revision history. You can also discuss and manage your project's work within the repository.

### Local Repository

It is the repo on which we will make local changes, typically this local repository is on our computer.

### Remote Repository

It is a common repository that all team members use to exchange their changes. In most cases, such a remote repository is stored on a code hosting service like GitHub or on an internal server.

### Cloning

Cloning a git repository means that you create a local copy of the code provided by developer; it is downloading the whole code of the repository.

### Issues

Issues are a great way to keep track of tasks, enhancements, and bugs for your projects. They're kind of like email—except they can be shared and discussed with the rest of your team.

### Branches

A branch is a parallel version of a repository. It is contained within the repository, but does not affect the primary or master branch allowing you to work freely without disrupting the "live" version. When you've made the changes you want to make, you can merge your branch back into the master branch to publish your changes.

### Master Branch

One word: the master branch is deployable. It is your production code, ready to roll out into the world. The master branch is meant to be stable, and it is the social contract of open source software to never, ever push anything to master that is not tested, or that breaks the build.

### Commit

It is a command used to save your changes to the local repository.

### Push

Pushing refers to sending your committed changes to a remote repository, such as a repository hosted on GitHub. For instance, if you change something locally, you'd want to then push those changes so that others may access them.

### Pull Request

Pull requests let you tell others about changes you've pushed to a branch in a repository on GitHub. Once a pull request is opened, you can discuss and review the potential changes with collaborators and add follow-up commits before your changes are merged into the base branch.

### Merge

It is a command which lets you take the independent lines of development created by git branch and integrate them into a single branch.
