---
title: 
tags: 
icon: 
aliases: 
---
- Blue/green deployment is a technique for releasing applications  by shifting traffic between two identical environments running different versions of the application
	- the **blue version** is the **currently running** version of the application
	- the **green** is the new version
- When youre satisfied that the green version is working properly, you can **gradually** reroute traffic from the old blue env to the new green environment .
- Blue/green deployments can mitigate common risks associated with with deploying software, such as:
	- downtime
	- rollback capability 