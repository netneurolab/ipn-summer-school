# Data science for neuroscience

(Or, "Project and data management: tips for the ~~lazy~~ industrious researcher")

This session will provide an overview of project + data management techniques + tools, with a focus on community-based standards.
There will be a practical demonstration of how to use [cookiecutter](https://cookiecutter.readthedocs.io/en/1.7.2/) to set up a project and a quick overview of how to use git/GitHub for version control.

## Requirements

You will need to have git installed on your local computer and a GitHub account in order to follow along with the demonstration!
(Also, to use these principles in the future, it's recommended you have a basic Python installation with at least cookiecutter installed.
Check the main README in the root of this repository for installation instructions!

## Recap

This section provides a brief recap of the basic cookiecutter + git/GitHub walkthrough we covered during the lecture.

First, we create a new cookiecutter project:

    cookiecutter https://github.com/drivendata/cookiecutter-data-science

This will prompt you for a bunch of information about the project; fill it out however you want!
For the purposes of this demonstration we'll assume the project is called `nnlab-intro-to-ds`.
(Note that this will raise a deprecation warning which can be safely ignored!)

Next, we navigate into the newly-created directory and initiate it as a git repository.

    cd nnlab-intro-to-ds
    git init

This may raise some warnings but should at the end say something like "Empty git repository intialized in <INSERT_PATH_HERE>".
Next we're going to rename the git branch we're on to `main` instead of `master` to keep up-to-date with current standards.
(We did not cover git branching in-depth during the tutorial because it is outside the scope of the workflow we covered but more information on branching can readily be found online.)

    git branch -m main

Next we're going to commit all the files + directories created by cookiecutter to git history:

    git add --all
    git commit -m 'Initial commit from cookiecutter'

Note that during class we just used the basic `git commit` command with no options, which opened a text editor like `vim` or `nano` where we typed the commit message.
The `-m '<MSG>'` flag here can be used instead to provide a commit message directly from the command line.

Now, go to GitHub and create a new repository by clicking the "+" in the top right corner of the page and select "Create new repository."
Fill out the name for the repository (we'll assume you use `nnlab-intro-to-ds` but you can use anything here).
Make sure that you leave all the boxes **unchecked** under the "Initialize this repository" heading!

Now, back on the command line, we can tell our local git repository about the GitHub repository:

    git remote add origin git@github.com:<username>/nnlab-intro-to-ds.git

Where you replace `<username>` with your GitHub username.

Next, we'll sync the local repository on your computer with GitHub:

    git push -u origin main

If you navigate to GitHub and refresh the page you should see all the files there!
Let's go back to your local repository and make some changes to a file:

    nano README.md
    # make some changes to the file and save it (in nano: `<ctrl+x>`, `y`, `<enter>`)

Check to see that `git` has identified the file was changed:

    git status

Now, add the file to prepare a commit, commit it, and then sync it with GitHub again

    git add README.md
    git commit -m 'Updated README.md'
    git push

These last three commands will be repeated *ad infinitum* for the remainder of the workflow.
As you change files and work on them you'll add them, commit them, and push them to GitHub!

## FAQ

### When I typed `git commit` it opened up a text editor in my console and I don't know how to exit! What do I do?

By default `git` uses `vim` as the command-line text editor.
To type your commit message press `i`, type your message, then hit `<Esc>`.
Next, type `:wq` and press `<Enter>` and you should be good to go!

If you would like to permanently change your git text editor to "nano" which is a bit more beginner-friendly you can use the following command:

    git config --global core.editor "nano"

### `git` is complaining that it doesn't know who I am. What do I do?

When `git` raises this error (likely after you trying and run `git commit` the first time) it should provide some information on the commands you need to run to fix it.
You will need to provide your name + email via the following commands:

    git config --global user.name "firstname lastname"
    git config --glboal user.email "email@domain.com"

Replacing with your own name and email!

## More questions?

Make an issue on this GitHub or email me at [ross.markello@mail.mcgill.ca](mailto:ross.markello@mail.mcgill.ca).
