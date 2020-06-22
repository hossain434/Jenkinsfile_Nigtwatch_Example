# Jenkinsfile_Nigtwatch_Example

1.	Please note - in the nightwatch.json file on Windows machine, update webdriver path to: "server_path": "./node_modules/chromedriver/lib/chromedriver/chromedriver.exe". It may work without .exe extension also.
2.	Install chrome browser on CentOS/Any machine: https://linuxize.com/post/how-to-install-google-chrome-web-browser-on-centos-7/
NPM chromedriver is a chromium driver which sends request to chrome browser, so both need to have on the host machine.
3.	Install Git on CentOS/Any machine: Follow this: https://linuxize.com/post/how-to-install-git-on-centos-7/
4.	In Jenkins, Install Git plugin then go to manage Jenkins -> Global tool configuration-> Git-> Name: Default, Check ‘Install automatically’ if you don’t have installed in your machine or virtual instance, Path to Git Executable: Git  
5. In Jenkins, go to manage Jenkins -> Global tool configuration-> NodeJS-> Name: node, Check ‘Install automatically’, select the version from dropdown and left the other fields as it is. Jenkins will take care NodeJS installation.  
6.	Create new Job: New Item -> Pipeline Script
7.	GitHub project: Project URL: https://github.com/hossain434/nightwatch_sample_example
8.	Pipeline: Definition-> Pipeline script form SCM

    SCM-> Git

    Repository URL: https://github.com/hossain434/nightwatch_sample_example  (doesn’t need to provide .git URL)

    Left the credentials blank since this is public link

    Branch to build: Master

    Repository browser: Auto

    Script path: Jenkinsfile

    Create a Jenkinsfile and add in the GitHub project. If you have more than one then name as Jenkinsfile_1, Jenkinsfile_2 etc.

    Example: https://github.com/hossain434/nightwatch_sample_example/blob/master/Jenkinsfile

9.	Build Trigger: Setup schedule.
