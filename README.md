## Instructions for Running Project ##

1. run 'docker-compose up --build' to start docker containers

2. cd to root directory hadoop to run commands
- you can run 'make-target' commands ('make event-counter' and 'make location_mapreducer' to aggregate jobs by location and events 
- hadoop should not be launched locally but through docker compose file and makefile commands

3. run 'make hadoop_solved' should produce solution
