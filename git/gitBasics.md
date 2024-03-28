## You will understand the basics of operating system and command lines

- **1. Operating System (OS):**

  ### **Definition:**

  - An operating system is a software that acts as an intermediary between computer hardware and the computer user. It manages hardware resources and provides services for computer programs.

  ### **Key Functions:**

  ### **a. Process Management:**

  - **Definition:**
    - Handles the execution of processes (programs in execution).
  - **Example:**

    ```java
    public class MyProgram {
        public static void main(String[] args) {
            // Code execution
        }
    }
    ```

  ### **b. Memory Management:**

  - **Definition:**
    - Manages computer memory, including RAM and storage.
  - **Example:**

    ```java
    int[] myArray = new int[10]; // Allocating memory for an array
    ```

  ### **c. File System:**

  - **Definition:**
    - Manages files and directories on storage devices.
  - **Example:**

    ```bash
    $ ls         // List files in the current directory
    $ mkdir MyFolder    // Create a new directory
    ```

  ### **d. User Interface:**

  - **Definition:**
    - Provides a user interface for interaction.
    - Can be graphical (GUI) or command-line (CLI).

  ### **e. Security:**

  - **Definition:**
    - Ensures data and system integrity.
  - **Example:**
    - User authentication and access control.

- **2. Command Line Interface (CLI):**

  ### **Definition:**

  - A command-line interface allows users to interact with the computer by typing commands into a text-based interface.

  ### **Basic Commands:**

  ### **a. Navigation:**

  - **Command:**

    ```bash
    $ cd [directory]
    ```

  - **Description:**
    - Change the current working directory.

  ### **b. Listing Files:**

  - **Command:**

    ```bash
    $ ls
    ```

  - **Description:**
    - List files and directories in the current directory.

  ### **c. Creating Directories:**

  - **Command:**

    ```bash
    $ mkdir [directory]
    ```

  - **Description:**
    - Create a new directory.

  ### **d. Copying Files:**

  - **Command:**

    ```bash
    $ cp [source] [destination]
    ```

  - **Description:**
    - Copy files from the source to the destination.

  ### **e. Removing Files and Directories:**

  - **Command:**

    ```bash
    $ rm [file]
    $ rm -r [directory]
    ```

  - **Description:**
    - Remove files or directories. The **`r`** flag is used for directories.

  ### **f. Text Editing:**

  - **Command:**

    ```bash
    $ nano [filename]
    ```

  - **Description:**
    - Open a text editor to create or edit a file.

  ### **g. Help:**

  - **Command:**

    ```bash
    $ man [command]
    ```

  - **Description:**
    - Display the manual (help) for a command.

### **Key Takeaways:**

- **Operating System (OS):**
  - Manages hardware resources and provides services for computer programs.
  - Key functions include process management, memory management, file system, user interface, and security.
- **Command Line Interface (CLI):**
  - Text-based interface for interacting with the computer.
  - Basic commands for navigation, file operations, and text editing.

---

## You will understand how to navigate directories using CLI

- **1. Present Working Directory (pwd):**

  ### **Command:**

  ```bash
  $ pwd
  ```

  ### **Description:**

  - Displays the current working directory.

- **2. List Contents of a Directory (ls):**

  ### **Command:**

  ```bash
  $ ls
  ```

  ### **Description:**

  - Lists the files and directories in the current working directory.

- **3. Change Directory (cd):**

  ### **Command:**

  ```bash
  $ cd [directory_path]
  ```

  ### **Description:**

  - Changes the current working directory to the specified directory.

  ### **Examples:**

  ```bash
  $ cd Documents         # Change to the "Documents" directory
  $ cd /path/to/directory    # Change to an absolute path
  $ cd ..             # Move up one level (parent directory)
  $ cd ~             # Change to the home directory
  ```

- **4. Navigate Back (cd with '..'):**

  ### **Command:**

  ```bash
  $ cd ..
  ```

  ### **Description:**

  - Moves up one level to the parent directory.

- **5. Navigate to Home Directory (cd with '~'):**

  ### **Command:**

  ```bash
  $ cd ~
  ```

  ### **Description:**

  - Changes the current working directory to the home directory.

- **6. Path Separators:**
  - In directory paths, the forward slash (**`/`**) is used as the path separator on Unix-based systems (Linux, macOS), while the backslash (**`\`**) is used on Windows.

### **Metaphor:**

- **Directory Navigation is like Exploring a Filing Cabinet:**
  - Imagine your computer as a filing cabinet. Each drawer is a directory, and each file is a document. The **`cd`** command is like opening a drawer to explore its contents, and **`ls`** is like taking a quick look inside.

### **Key Takeaways:**

- **`pwd`**: Display the current working directory.
- **`ls`**: List contents of the current directory.
- **`cd [directory]`**: Change to the specified directory.
- **`cd ..`**: Move up one level (parent directory).
- **`cd ~`**: Change to the home directory.

---

## You will understand how to manipulate files using CLI

- **1. Creating a File (touch):**

  ### **Command:**

  ```bash
  $ touch [filename]
  ```

  ### **Description:**

  - Creates an empty file with the specified filename.

- **2. Copying Files (cp):**

  ### **Command:**

  ```bash
  $ cp [source] [destination]
  ```

  ### **Description:**

  - Copies a file from the source location to the destination.

- **3. Moving/Renaming Files (mv):**

  ### **Command:**

  ```bash
  bashCopy code
  $ mv [old_filename] [new_filename]

  ```

  ### **Description:**

  - Renames a file or moves it to a different location.

- **4. Removing/Delete Files (rm):**

  ### **Command:**

  ```bash
  $ rm [filename]
  ```

  ### **Description:**

  - Removes (deletes) the specified file.

- **5. Displaying File Content (cat):**

  ### **Command:**

  ```bash
  $ cat [filename]
  ```

  ### **Description:**

  - Displays the content of the specified file.

- **6. Editing Files (nano):**

  ### **Command:**

  ```bash
  $ nano [filename]
  ```

  ### **Description:**

  - Opens a text editor to create or edit a file.
  - To save changes and exit Nano, press **`Ctrl + X`**, then press **`Y`** to confirm, and finally, press **`Enter`**.

- **7. File Permissions (chmod):**

  ### **Command:**

  ```bash
  $ chmod [permissions] [filename]
  ```

  ### **Description:**

  - Changes the permissions of a file.

  ### **Example:**

  ```bash
  $ chmod +x script.sh
  ```

  - This command gives execute permissions to a script.

### **Metaphor:**

- **File Manipulation is like Crafting and Organizing Documents:**
  - Imagine your computer as a desk with various documents (files). You can create new documents, copy them, move them to different drawers (directories), and even modify their content with various tools (editors).

### **Key Takeaways:**

- **`touch [filename]`**: Create an empty file.
- **`cp [source] [destination]`**: Copy a file.
- **`mv [old_filename] [new_filename]`**: Move or rename a file.
- **`rm [filename]`**: Remove/delete a file.
- **`cat [filename]`**: Display file content.
- **`nano [filename]`**: Edit a file.
- **`chmod [permissions] [filename]`**: Change file permissions.

---

## You will understand how to initialize a GIT repository

- How to Get a Git Repository

  There are two ways of obtaining a Git repository:

  - Turning an existing directory into a Git repository (initializing).
  - Cloning a Git repository from an existing project.

- Initialize a Repository

  To initialize a Git repository in an existing directory, start by using the Git Bash terminal window to go to your project's directory:

  ```bash
  cd [directory path]
  ```

  Where [directory path]: The path to your project directory.

- Use Git Bash to go to your project directory

  Once you navigate to the project directory, initialize a Git repository by using:

  ```bash
  git init
  ```

- Initializing a Git repository with git init

  Initializing a repository creates a subdirectory called .git that contains the files Git needs to start tracking the changes made to the project files. The repository only starts tracking project versions once you commit changes in Git the first time.

- Clone a Repository

  Use the git clone command to clone an existing repository and copy it to your system:

  ```
  git clone [url] [directory]
  ```

  Where:

  [url]: The URL of the Git repository you want to clone. [directory]: The name of the directory you want to clone the repository into. Note: specifying the directory is optional; if not specified it will clone to the current directory.

## You will be able to explain the GIT workflow

**Git Workflow is like Collaborative Storytelling:**

- Imagine your project is a storybook. Cloning is getting a copy of the book. Editing and staging changes are like preparing new chapters. Committing is adding those chapters to the story. Pushing is sharing your changes with others, and pulling is getting the latest chapters from others.

### **Key Takeaways:**

- **`git clone`**: Clone a remote repository.
- **`git status`**: Check the repository status.
- **`git add`**: Stage changes for commit.
- **`git commit`**: Record changes with a commit message.
- **`git push`**: Upload local commits to the remote repository.
- **`git pull`**: Fetch and merge changes from the remote repository.
- **`git branch`**: Create a new branch.
- **`git checkout`**: Switch to a different branch.
- **`git merge`**: Combine changes from one branch into another.
- Git Merge

  Merging is Git's way of putting a forked history back together again. The git merge command lets you take the independent lines of development created by git branch and integrate them into a single branch.

  Note that all of the commands presented below merge into the current branch. The current branch will be updated to reflect the merge, but the target branch will be completely unaffected. Again, this means that git merge is often used in conjunction with git checkout for selecting the current branch and git branch -d for deleting the obsolete target branch.

- How it works

  Git merge will combine multiple sequences of commits into one unified history. In the most frequent use cases, git merge is used to combine two branches. The following examples in this document will focus on this branch merging pattern. In these scenarios, git merge takes two commit pointers, usually the branch tips, and will find a common base commit between them. Once Git finds a common base commit it will create a new "merge commit" that combines the changes of each queued merge commit sequence.

- New merge commit node

  Merge commits are unique against other commits in the fact that they have two parent commits. When creating a merge commit Git will attempt to auto magically merge the separate histories for you. If Git encounters a piece of data that is changed in both histories it will be unable to automatically combine them. This scenario is a version control conflict and Git will need user intervention to continue.

- Preparing to merge

  Before performing a merge there are a couple of preparation steps to take to ensure the merge goes smoothly.

  - Confirm the receiving branch
    - Execute git status to ensure that you are pointing to the correct merge-receiving branch.
    - If needed, execute git checkout to switch to the receiving branch. In our case we will execute git checkout main.
  - Fetch latest remote commits
    - Make sure the receiving branch and the merging branch are up-to-date with the latest remote changes.
    - Execute git fetch to pull the latest remote commits.
    - Once the fetch is completed ensure the main branch has the latest updates by executing git pull.

---

## You will understand how to resolve merge conflicts

- **1. Understanding Merge Conflicts:**
  - A merge conflict occurs when Git is unable to automatically merge changes from different branches. This often happens when changes are made to the same part of a file in both branches.
- **2. Checking for Conflicts:**

  ### **Command:**

  ```bash
  $ git status
  ```

  ### **Description:**

  - Shows files with conflicts and unmerged changes.

  ### **Example:**

  ```bash
  $ git status
  On branch main
  You have unmerged paths.
    (fix conflicts and run "git commit")
    (use "git merge --abort" to abort the merge)
  Unmerged paths:
    (use "git add <file>..." to mark resolution)
          both modified:   myfile.txt
  ```

- **3. Opening the Conflicted File:**
  - Open the conflicted file in a text editor. Git marks the conflicting sections with special markers like **`<<<<<<<`**, **`=======`**, and **`>>>>>>>`**.
- **4. Resolving Conflicts Manually:**

  - Edit the conflicted file to choose which changes to keep. Remove the conflict markers and make the file consistent.

  ### **Example:**

  ```
  <<<<<<< HEAD
  This is the current change in the main branch.
  =======
  This is the conflicting change from the feature branch.
  >>>>>>> feature-branch
  ```

- **5. Marking as Resolved:**

  ### **Command:**

  ```bash
  $ git add [conflicted_file]
  ```

  ### **Description:**

  - Marks the conflicted file as resolved.

- **6. Completing the Merge:**

  ### **Command:**

  ```bash
  $ git merge --continue
  ```

  ### **Description:**

  - Completes the merge process after resolving conflicts.

- **7. Aborting the Merge:**

  ### **Command:**

  ```bash
  $ git merge --abort
  ```

  ### **Description:**

  - Cancels the merge and restores the repository to the state before the merge.

### **Metaphor:**

- **Resolving Merge Conflicts is like Editing a Shared Document:**
  - Imagine working on a document with a friend. If you both edit the same sentence, you need to decide which version to keep. Git conflict markers are like highlighters showing where changes clash.

### **Key Takeaways:**

- Conflicts arise when Git cannot automatically merge changes.
- Use **`git status`** to check for conflicted files.
- Open the conflicted file, resolve conflicts manually, and remove conflict markers.
- Use **`git add`** to mark the file as resolved.
- Complete the merge with **`git merge --continue`**.
- If needed, abort the merge with **`git merge --abort`**.
