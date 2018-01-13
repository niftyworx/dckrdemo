Setup your local post-commit local hooks

======OS
jdo@jdo-ub1604:~/github_repo/dckrdemo$ cat .git/hooks/post-commit 
#!/bin/sh

curl --user admin:<api_token_from_jenkinuser> http://localhost:8080/job/dockerdemojob/build?token=<custom_tokenname_given_in_the_job>

/home/jdo/github_repo/dckrdemo/buildExecutable

echo "Executed from post-commit hook"

=======Jenkin Job
Source Code Management
 > Git

Build Triggers
 > Trigger builds remotely (e.g., from scripts) - name your token



