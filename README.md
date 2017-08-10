# Skopos Surveyor
A free tool for Docker users that scans, discovers and displays all your running applications and their architecture. It works with single-host Docker systems as well as with Docker swarm clusters. In about 3 minutes, you can download, install and discover your running applications producing a nice picture you can share with the rest of the team. 

![alt text](http://opsani.com/wp-content/uploads/2017/08/Architecture-768x539.png "Skopos Surveyor Architecture Visualized")

- Discover What’s Running In Minutes: Skopos Surveyor scans your Docker host or Swarm manager node to quickly show you what you have running.
- Visualize Your Architecture - Once you’ve discovered your applications, Skopos Surveyor gives you new insight by visualizing service architecture, making it easy to see relationships and dependencies.
- Share with Anyone - With visual architecture you can easily share context with other teams members without them having to scan through reams of code.
- Save Your Architecture As Code - Beyond the visuals, Skopos Surveyor codifies your architecture saving it as a YAML file that can be checked into your source repo and used by others.

[Visit the Opsani website for additional details.](http://opsani.com/surveyor)

## Install

Run the Skopos container on the same machine that hosts your applications:
– On a single Docker host, run this command on that host
– On a Docker Swarm cluster, run this command on the manager node

```docker run -d -p 8100:8100 --name skopos -v /var/run/docker.sock:/var/run/docker.sock opsani/skopos:edge```
  
## Run
Open your browser to ```http://localhost:8100```
Note: replace ```localhost``` with the actual host or IP address where Skopos runs.

![Surveyor Main Screen](http://opsani.com/wp-content/uploads/2017/08/Discover1-1-610x427.png "Surveyor Main Screen")

Click the ```Discover Existing Applications``` option to scan your running applications. 

Discovery usually completes in 20-30 seconds though the first time may take a minute or more so that we can load the Surveyor helper containers. Also, if you want to capture the right connections between services, exercise your application during the discovery so we can see the traffic.

This will produce a list of applications including a ```Discover_all``` that shows everything found in one screen.

![AppList](http://opsani.com/wp-content/uploads/2017/08/AppList-610x428.png "Application List")

Click on your specific application to view the architecture diagram.
![Architecture](http://opsani.com/wp-content/uploads/2017/08/Architecture-768x539.png "Architecture")

## Save

Use the print-screen or Print to PDF option in your browser to share this picture with others on your team.

Click the ```{}``` icon in the upper right of the screen to see the picture (i.e. Model) in YAML.

![YAML](http://opsani.com/wp-content/uploads/2017/08/ArchitectureAsCode.png "YAML")

Check the YAML and/or picture into your source repository as a record of the current architecture.

## Discover Future Apps

Run the Discover again if you need to see new apps that are up and running by going to the app list and selecting ```Discover Applications```

![AppList](http://opsani.com/wp-content/uploads/2017/08/AppList-610x428.png "Application List")

## Feedback 
Let us know what you think of Skopos Surveyor [here](https://docs.google.com/forms/d/e/1FAIpQLSde6eEqJlOV-VzcpX_8kRTySurjgLbNlTuiDUbdSeNsEOcHDQ/viewform?usp=sf_link).
