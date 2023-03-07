# JAVAFX
## General info
Framework for java GUI's

To have FX, you need Oracle JDK8 (not openJDK 8) so that it's included.

The main class for a JavFX application is the javafx.application.Application class.
Extend this and override start() method to begin the program.
Usually, the launch(args) in main does nothing. JVM starts from start?

	public class MyJavaFX extends Application {
		@Override 
		public void start(Stage primaryStage){
			// start code here
			Button btOk = new Button("Ok");
			Scene scene = new Scene(btOk, 200, 250);
			primaryStage.setTitle("myScene");
			primaryStage.setScene(scene);
			primaryStage.show();
		}
	}

FX defines the UI container by means of a stage and a scene.
The Stage class is the top level FX container. Think of it as a stage on which 
the play occurs. It's a window on our screen.
The FX Scene class is the container for all content. think of it as a scene in a play
Nodes are the actors to perform in the scene.

An object of our class is created in the JVM, Stage is created and start is run

Stage contains Scene(s) which contains StackPanes? root? TODO more on this...

The root node (instance of StackPane) is crated and passed to scene constructor,
along with W/H

See slide for diags

Root node begins a tree graph that represents everything in a scene.


