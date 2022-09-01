## CI-CD
- CICD is a set of practices that create a CICD pipeline, which allows us to have our latest version of the developed software to be integrated and deployed automatically to our production environment, or to the customers directly.




## Continuous Integration (CI): 
Developers merge/commit code to master branch multiple times a day, fully automated build and test process which gives feedback within few minutes, by doing so, you avoid the integration hell that usually happens when people wait for release day to merge their changes into the release branch.


## Continuous Delivery :
It is an extension of continuous integration to make sure that you can release new changes to your customers quickly in a sustainable way. This means that on top of having automated your testing, you also have automated your release process and you can deploy your application at any point of time by clicking on a button. In continuous Delivery the deployment is completed manually.

## Continuous Deployment: 
It goes one step further than continuous delivery, with this practice, every change that passes all stages of your production pipeline is released to your customers, there is no human intervention, and only a failed test will prevent a new change to be deployed to production.

## jenkins:
- It is a tool to implement the CICD pipeline. It automates the processes the developed software have to be gone through before production and the deployment to the pre-production/production environment.

## Testing webhook



image.png

CI-CD.png

Steps:
- Create a new Repo on github
- initialise that repo on local host by ssh
- push app folder using ssh method to the git repo
  
- If you have an error related to repo does not exist, then run following commands
- eval "$(ssh-agent -s)"

- ssh-add ~/.ssh/122

- git push -u origin main

- Now refresh the git account page and the file will be there.

 OR

- Visit your GIT-with-SSH repo on your github account
  
- Now, you'll have app folder and README file in your git repo, pushed from local host using ssh
  
- Now, in order to communicate between Jenkins and Github, we need ssh keys
- To create new keys:
- Go to .ssh folder from git terminal
- Inside .ssh folder run following command
- ssh-keygen -t rsa -b 4096 -C "your_email@example.com" (change email to your git email)
- When you press enter it'll ask for the name of the key, Give name of the key ex:Jenkins122
- After that it'll ask for password, if you don't want to set password then simply press enter
- Again will ask to confirm password, press enter
- Now it'll create the keys
- run 'ls' command and you'll be able to see your keys 'Jenkins122.pub' and 'Jenkins122'

- Now, we need to copy and paste public key (Jenkins122.pub) to our git repo and paste the private key (Jenkins122) into the Jenkins Configuration.
  
  - Run 'cat Jenkins122' and it will show the content of the key, copy whole of it and go to your repo which needs to be connected to Jenkins,
  - Go to settings option of that repo and on the left click on the deploy keys and click on the add deploy key
  - Then paste the public key and give the same name to the key and click on read and write permission
  - click add the key

image.png

