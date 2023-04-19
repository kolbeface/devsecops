# devsecops
A repository of notes, study tools and a CI/CD Pipline Project

Current Strugle:
take a look at actions tab at the workflow Docker Image CI K8s CD
this is the file: docker-image.yml
the scope of the issues lies on lines 46-62
Everything works great and as expected in this workflow, I have multiple lines of troubleshooting going on and they all work great, the problem lies on line 61.  All of this is my first experience so if something looks really weird I apologize.  Basically I am version controlling my docker file initialized on line 27 with the TAG variable.  I am uploading a docker image with that tag to docker hub.  This works perfectly.
I then pass the variable to the next job and set it as an environment variable on line 52. again vie debugging I can confirm that this is working.  
I have read some documentation that says all i need to do is set environment variables and then i can use them in an external file, others tell me to use the export command, you can see i try both.
On line 56 i verify that I can access my k8 pods this works as it should
on line 61 i try to apply my deployment this can be found in directory k8s.
From what I read all i need to do is image: kfface/shepokes-site:${{ env.TAG }} (found on line 29 of ./k8s/shepokes-depl1.yaml)
if i hard code the docker tag it works as it should, when i use this env.TAG it does not work. 
