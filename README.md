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
