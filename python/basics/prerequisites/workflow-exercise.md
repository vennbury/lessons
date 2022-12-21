---
title: "Exercise: Practicing Workflow"
priority: "4"
unit: "prerequisites"
lesson: "workflowExercise"
next: "basics/python-basics"
---

# Practicing Your Workflow

This exercise is a foundation of your workflow for the whole course. You will practice creating GitHub repositories, cloning them on your computer, creating files with CLI, adding them to the stage area, committing, and pushing all of the changes to GitHub.

## Exercise

- Step 1: Assuming you're logged in to your [GitHub](https://github.com) profile, create a new repository and name it "Workflow". For now, ignore README, .gitignore, and license settings (you will learn more about them further into your developer career).
- Step 2: GitHub should show you a couple of ways to connect your local git to GitHub. On top, you should see a blue box with the heading like this: "Quick setup — if you’ve done this kind of thing before". There are two buttons, "HTTPS" and "SSH". Click on the latter and copy the line. (It should look like this: "git@github.com:[your-user-name]/workflow.git".)
- Step 3: Open up your OS's CLI.
- Step 4: Navigate into the desired folder, where you'll be storing all of your exercise and project folders, using `cd` command.
- Step 5: Type in `git clone ` and paste the copied SSH key from Step 2. (Usually, `Ctrl + V` doesn't work in CLIs. Try `Ctrl + Shift + V`. Alternatively, you can manually type the SSH key.)
- Step 6: Use `ls` command (or your OS's alrernative) to see whether the folder was added. After, navigate into it.
- Step 7: Create a file named `first.py` and open it with `code .`. (Technically, you open the folder, not the file, but it doesn't matter for our purposes.)
- Step 8: Write `print('Hello, world!')` in that file and save it using `Ctlr + S`.
- Step 9: Now you need to add the file to the staging area, commit it, and push it to the repository. You have two ways of doing it: via CLI and via VS Code. We <b>highly</b> recommend using the second way at least until the end of the Basics course, because you need to practice CLI. However, we will show you both: Steps 9.1 pertain to CLI, while 9.2 - to VS Code.
- Step 9.1.1: In your CLI, type `git status`. It will show you the changes made in files.
- Step 9.1.2: Type `git add -A`. This command adds all of the files into a staging area. Type `git status` again and check that the file were, in fact, added there.
- Step 9.1.3: Type `git commit -m "First commit"`. This command makes a commit to the repository. The commits, however, stay on your local machine until you push them into the repository. (Type `git status` to see that the files are not in the staging area anymore.)
- Step 9.1.4: Type `git push origin main` to push the changes into GitHub. (You might have the main branch called "master", in which case you should change the last word in the command accordingly.)
- Step 9.1.5: Go to the GitHub repository you created for this exercise and refresh the page. You should see the changes reflected here.
- Step 9.2.1: In your VS Code, the third button on the vertical bar on the left is your source control tab. Click on it.
- Step 9.2.2: Click on a "+" button to add the file to the staging area.
- Step 9.2.3: Write "First commit" in the textbox on top and click the "commit" button right below it.
- Step 9.2.4: Refresh your GitHub repository and you should see your `first.py` file there.

## Conclusion

Follow this workflow for each exercise and project that requires you to set up your own repository.
