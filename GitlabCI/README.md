## Домашняя работа к занятию “ CI/CD”


```
Running with gitlab-runner 14.2.0 (58ba2b95)
 on netologyRun uX3Cyknb
Preparing the "shell" executor
Using Shell executor...
Preparing environment
Running on main.localdomain...
Getting source from Git repository
Fetching changes with git depth set to 50...
Reinitialized existing Git repository in /home/gitlab-runner/builds/uX3Cyknb/0/root/netology/.git/
Checking out 9020b1fd as main...
Skipping Git submodules setup
Executing "step_script" stage of the job script
$ mkdir /home/gitlab-runner/builds/build
$ touch /home/gitlab-runner/builds/build/info.txt
$ echo "Compile complete."
Compile complete.
Job succeeded
```

```Running with gitlab-runner 14.2.0 (58ba2b95)
  on netologyRun uX3Cyknb
Preparing the "shell" executor
Using Shell executor...
Preparing environment
Running on main.localdomain...
Getting source from Git repository
Fetching changes with git depth set to 50...
Reinitialized existing Git repository in /home/gitlab-runner/builds/uX3Cyknb/0/root/netology/.git/
Checking out 9020b1fd as main...
Skipping Git submodules setup
Executing "step_script" stage of the job script
$ echo "Testing"
Testing
$ test -f /home/gitlab-runner/builds/build/info.txt && echo "$FILE Существует"
 Существует
Job succeeded