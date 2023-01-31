# How to Contribute

## Step 1: Fork this repository

Fork this repository by clicking on the `fork` button located on the top of this page. This will create a copy of this repository in your account.

## Step 2: Clone the repository

Find the lessons repository you just forked on your personal github. On the top right, click the green `<> Code` button and coppy the link. Now open a terminal
on your local machine, navigate to the directory you would like this repository to be located in and type:

```
git clone [copied URL]
```

## Step 3: Create a branch

On your local computer, navigate to the lessons repository directory. Now create a new branch with the following command:

```
git switch -c [branch_name]
```

## Step 4: Make your changes

Navigate to the lesson(s) you want to change in the lessons folder. The folders follow the same structure that the website follows, except that the folder is named lessons and not courses.

## Step 5: Push your changes

After making your changes, you will push your changes to github. To do so, in your local terminal type the following:

```
git add .
git commit -m "[your_message]"
git push -u origin [branch_name]
```

## Step 6: Making a pull request

On Github, locate the lessons repository you cloned and just pushed to. Click on the `Compare & pull request`, fill out the necessary information, and click `create pull request` to submit your changes.
