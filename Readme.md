Technical Assessment


1. Running the command curl google.com command from docker container: 

    I am not able to curl google.com from docker container as there are firewall issues with the container and unable to connect to the internet.

2. The circleci/challenge-2 container image is meant to serve up a very simple "Hello World!" website at port 8000. If you run the container with docker run circleci/challenge-2 and then visit localhost:8000, can you see the site? If not, can you figure out how to make it work?
    Yes I can see the site on localhost:8000
   ![image](https://user-images.githubusercontent.com/57142156/191133396-9e8509fc-3966-49e3-b0ff-9974d203756a.png)
3. The circleci/challenge-3 image also serves the same simple website. This time, it is served by nginx on port 80. The desired behavior is for the "Hello World!" site to be displayed, NOT the default "Welcome to nginx!" site. Can you see the correct site at http://localhost? If the wrong one is being displayed, can you fix it? You might find it useful to "log in" to the container by running docker exec -it <container name or id> bash once it is running and taking a look around.
	 For this task, I changed the index.html page (location: usr/share/nginx/html) to hello work (simple html text)
	![image](https://user-images.githubusercontent.com/57142156/191133737-c07930bd-354f-4200-9857-29f104acbb33.png)
4. This container should start up with a few long-running processes. Some of these processes are using quite a bit of memory. Which ones? Can you figure out how they got started? Can you stop them all? (Again, you'll probably want to use docker exec to get access to the running container.)
	  
	 For this task we can exec inside the container and run the Top command to see the running processor. Also we can use free -mem (specific to memory) command to the available and used memory. Then I used Kill -9 command to stop the processors and that leads to more available memory.
	
	 ![image](https://user-images.githubusercontent.com/57142156/191133834-ca088d0c-1be4-4ab1-98a5-e4f3f7659555.png)
	
Build and Test
1. Using any language or framework, make a trivial web application that contains a single page with a button. When you click on this button the page should display some new text (HTML and basic JavaScript is enough).
     The index.html file is created.

2. Write a test to ensure that the new text is displayed when the button is clicked.
   Go to index.html --> click on on-click button --> output: "Hey you clicked me!, it's CricleCI assessment thanks!"
	


	
	
	
	


