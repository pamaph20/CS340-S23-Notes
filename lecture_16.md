<<<<<<< HEAD
Lecture 16
Install : openjdk-19-jdk-headless and maven 
Sudo apt install "the thing you want to install" 

Fork from repo 
Clone : git clone "what you forked " 


Continuous Integration 
	- Frequent merging or rebasing to main 
	- Automatically test this new commit 

Continuous Delivery / Deployment 
	- Delivery is package up code to deploy /release 
	- Probably don't want to deploy to all users all at once 
		○ High risk if something goes wrong 
		○ Deploy to small subset of users 
			§ Canary Deployment 
		○ Gradually roll out the deployment 
			§ Rolling Deployment
				□ Some people get the feature before you get the feature 
			§ Blue Green Deployment 
				□ Blue is the old deployment and blue is the new deployment 
				□ Cutover - where you switch people from one deployment to another 
Challenge - CI/ CD requires frequent commits and frequent deployments
	- Feature Development / refactoring can take a long time 
		○ Longer than the commit/push/deploy pipeline 
		○ Idea : break feature into small chunks 
			§ The feature is broken or doesn't work …
			§ CI/CD deploys this to this end user 
			§ How do we handle broken changes being deployed without breaking the code for the user 
=======
Fill in lecture 16 notes 
>>>>>>> main
