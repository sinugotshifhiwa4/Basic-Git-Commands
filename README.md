# Basic-Git-Commands

## Pushing a Project to a New Repository

To push an existing local project to a new GitHub repository, follow these steps:

1. **Create a repository** on GitHub and copy the repository URL.
2. Open the terminal in your local project directory.
3. Initialize Git in the project:
   ```sh
   git init
   ```
4. Check the current status:
   ```sh
   git status
   ```
   - If you **did not** create a README file in GitHub, skip to step 7.
5. Connect the local repository to the remote GitHub repository:
   ```sh
   git remote add origin <repository-url>
   ```
6. If you created a README file in GitHub, first pull the latest changes:
   ```sh
   git fetch origin
   git pull origin <your-branch>
   ```
7. Add all project files to Git tracking:
   ```sh
   git add .
   ```
8. Commit the changes:
   ```sh
   git commit -m "Initial commit"
   ```
9. Connect the local repository to the remote GitHub repository (if not already connected in step 5):
   ```sh
   git remote add origin <repository-url>
   ```
10. Push the project to the remote repository:
   ```sh
   git push -u origin <branch>
   ```

Now your project is successfully pushed to GitHub!

## Removing a Committed Folder from Remote Repository

If you have accidentally committed a folder and want to remove it from tracking:

```sh
git rm -r --cached <folder name>
```

Commit the changes:

```sh
git commit -m "Removed <folder name> folder from Git tracking"
```

Push the changes to the remote repository:

```sh
git push -u origin <your-branch>
```

## Pulling the Latest Changes from the Remote Repository

To update your local repository with the latest changes from the remote:

```sh
git fetch origin
```

Then merge the changes:

```sh
git pull origin <your-branch>
```
