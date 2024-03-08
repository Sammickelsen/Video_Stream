# Overview

Networking as a whole has always been difficult for me to understand, so I decided to work on a project which allowed me to really hone the basics of the topic.  I wanted to build some sort of video sharing service using a peer-to-peer connection.  I found a good package that allowed me to focus on the higher-level understanding behind ports and networking as a whole.

The program has a simple GUI built in using Tkinter, Pythons built-in GUI package, which gives the user a few options.  First the user must type in the IP of the user they wish to stream video to.  The other user needs to do the same.  Then a user can click listen to start listening for information from that IP.  The other user can then choose one of the three options given to them; video stream, screen share, or audio stream.  The users can follow the same logic to get both of their video, audio, and screen sharing working at the same time.  It is a clunky way of doing it for now, but can easily be changed in the future if needs be.

{Provide a link to your YouTube demonstration.  It should be a 4-5 minute demo of the software running (you will need to show two pieces of software running and communicating with each other) and a walkthrough of the code.}

[Software Demo Video](https://youtu.be/CMNGvEAgaus)

# Network Communication

I decided to work with peer-to-peer connection, since I have done more client/server in the past.  I wanted to get a better feel for the peer-to-peer connections.  I thought it would be simpler than client/server, and in some ways it was, but in others I ran into hiccups.

I am using UDP, which is why my code has both a server and a receiver.  One to listen and one to send information.  I am using ports 9999, 8888, 7776, 6665 between the two programs in order to connect to each other.

Since my program is sending both vidoes and audio, the format of the messages being sent between peers is different depending on what is running.  We could be passing compressed audio data, video frames (in the form of image files), or compressed video files based on which function is currently running.

# Development Environment

I used VSCode as my workspace of choice.

I coded in Python, using the Tkinter for the GUI. I used socket, threading and Vidstream libraries to help with the networking side of things.

# Useful Websites

* [Medium: How To Make Your Own Streaming Video Sharing App Using Python](https://medium.com/geekculture/how-to-make-your-own-streaming-video-sharing-app-using-python-481437262fe9)
* [Screen Sharing Tutorial](https://www.youtube.com/watch?v=8xy4JKvqsV4)

# Future Work

* Streaming Data does not stop until user quits out of the program entirely. I need to be able to quit out of program easily.
* Make the UI nicer and easier to use.  Many users won't understand how to connect as it is now.
* Make it so that a user can't continuously open windows on the other user's computer.