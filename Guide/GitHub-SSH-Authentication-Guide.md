# A Step-by-Step Guide to GitHub SSH Authentication

If you want to use GitHub without typing your password every time, you can set up SSH authentication. This guide will show you how to do it step by step.

## Step 1: Install Git
First, you need to install Git. If you are using Ubuntu or a similar system, run this command:

```bash
sudo apt install git
```

## Step 2: Set Up Your Name and Email
Git needs to know who you are. Set your name and email like this:

```bash
git config --global user.name "Your Name"
git config --global user.email "Your Email"
```

Replace "Your Name" and "Your Email" with your actual details.

## Step 3: Create an SSH Key
To connect to GitHub securely, you need an SSH key. Create one by running:

```bash
ssh-keygen -t ed25519 -C "Your Email"
```

This generates a key that allows you to connect to GitHub safely.

Next, display the key:

```bash
cat ~/.ssh/id_ed25519.pub
```

Copy the output and add it to GitHub. Go to **Settings > SSH and GPG keys** on GitHub and paste the key.

## Step 4: Test the SSH Connection
Check if your SSH key is working by running:

```bash
ssh -T git@github.com
```

If everything is set up correctly, you’ll see a welcome message from GitHub.

## Step 5: Start a New Git Project
Go to your project folder and set up Git:

```bash
cd directoryname/
git init
```

This tells Git to track your project files.

## Step 6: Connect Your Project to GitHub
Now, link your project to a GitHub repository:

```bash
git remote add origin git@github.com:username/repo.git
```

Replace `username` with your GitHub name and `repo.git` with your repository name.

## Step 7: Add and Upload Files
First, add your files to be saved:

```bash
git add .
```

Then, save the changes with a message:

```bash
git commit -m "Adding files"
```

Rename the default branch to `main`:

```bash
git branch -m main
```

Now, send your files to GitHub:

```bash
git push -u origin main
```

## Step 8: Fetch and Update Your Files
To check for updates from GitHub, run:

```bash
git fetch origin
```

To update your local files with the latest changes:

```bash
git pull origin main --rebase
```

Finally, to send any new changes to GitHub:

```bash
git push origin main
```

By following these steps, you can connect to GitHub using SSH and work with your repositories easily without entering your password every time.

