# Game of Three

## How to run the program

* This is a maven project, use any IDE and import as Maven project
* Execute `mvn clean install`
* Under **target** folder, two jars would be created - **client.jar** & **server.jar**
* Run both the jars in two different terminals using below commands:


    java -jar server.jar
    java -jar client.jar


* Results would be printed on console

Notes:
1. This game is designed to be played by 1 Sever Player and 1 Client Player at a time. 
2. Select the playing mode: 0- Auto   1- Manual. Manual is an interactive mode to take inputs from user.

## Documentation
This application simulates the Game of Three. It is played between two players talking over a network. 
It is like a client-server interaction. One player starts the game and waits till another player joins. The program 
exits when a player receives 1 as the message and is declared winner. 
Details on how to play the game can be read: Game of Three - 
Scoober Integrations Team - Backend Coding Challenge JAVA.pdf


The application is modularized into number of classes having specific methods and business logic. The details about 
classes are as below:

### ClientApplication.java

This class acts as a player which when started listens for server and connects with a handshake. If server is not 
present, it waits. This class extends `WebSocketClient` and joins a websocket connection of the server.

### ServerApplication.java

This class acts as a player which when started waits for other player(client). As soon as the client joins, it sends a 
random number to client and starts the game. This extends `WebSocketServer` and opens a websocket connection for client 
to join.

### InputUtil.java

Contains utility method used in the application.

### Constants.java

Contains application constants.







