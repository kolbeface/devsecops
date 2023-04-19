# devsecops
A repository of notes, study tools and a CI/CD Pipline Project

This CI/CD pipeline takes any changes done to ./app and builds an updated version of the container. The container is then taged it with a version controled date/time and the updates are pushed to kfface/shepokes-site which is stored on hub.docker.com.  Once that is complete it pulls the new image and integrates it with my kubernetes cluster which is hosted on digitalocean.com. No downtime of the website is experienced thanks to the k8s load balancer and updates are pushed live within a few seconds (under 1 minute from initiation of pull request under 16 seconds from kubernetes deployment update).
