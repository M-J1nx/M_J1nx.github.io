# Why can’t I make contributions even if I did commit?

In github, there is **contributions** map which shows contributions of the year. 

Many programmers try to fill this map by doing one commit per one day.

But I’ve got a trouble that some commits I made wasn’t displayed in contributions map. 

Following is method that I’ve tried to figure this out. 

First, you should find `.gitconfig` file. This would place where `Git` had been installed or `User` folder in `C drive` . 

You can find user infomation when you open it. 

Following information should be matched with :

- name : github account name
- email : github email

![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/8a656925-fc0e-4de1-9947-61a6517e8bb1/093dc8de-91d0-4fb0-823c-402e41c61d6f/image.png)

![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/8a656925-fc0e-4de1-9947-61a6517e8bb1/84f094b8-9326-4304-a785-c0ec159b4f39/image.png)

After saving this, you can check that your commit is shown in contribution map.

If you can’t see, please check if your commits meet the conditions from the following : 

https://docs.github.com/ko/account-and-profile/setting-up-and-managing-your-github-profile/managing-contribution-settings-on-your-profile/why-are-my-contributions-not-showing-up-on-my-profile

- The email address used for the commits is associated with your account on GitHub.
- The commits were made in a standalone repository, not a fork.
- The commits were made:
    - In the repository's default branch (If you commit to branch which is not default, that won’t be shown in contribution. You should create pull request or merge your branch into default branch)
    - In the `gh-pages` branch (for repositories with project sites)