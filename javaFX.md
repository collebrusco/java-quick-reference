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

can make a grid node with 

	GridPane grid = new GridPane();
	// pass to scene as root 

Let's make a 3x3 grid and add some orange rectangle outlines

	for (int i = 0; i < 3; i++){
		for (int j = 0; j < 3; j++){
			Shape sh = new Rectangle(100, 100);
			sh.setFill(null);
			sh.setStroke(Color.ORANGE);
			grid.add(sh, i, j);
		}
	}
	
Other shapes... google em!

But we want to interact. Eventhandlers are here

EventHandler: class with a handle() method (functional interface)

register an eventhandler with something that can create events, it'll call handle when the event occurs

handle() is then a callback subroutine (listener)
we're gonna usually have eventhandlers be anon classes, defined inline to access variables within the scope of interest

Lets look at code to add a button that does something

	Button b = new Button("Randomize");
	grid.add(b, 0, 2);
	button.setOnAction(new EventHandler<ActionEvent>(){
		@Override
		public void handle(){
			// do some random stuff
		}
	});

Now button will call handle() when pressed, the anon class acts almost as a lambda but for entire classes instead of funcs.
Could pass a regular named extension of EventHandler<ActionEvent>() if needed, usually you dont, benifit of not is accessing local vars (instance vars)
Anon classes still get .class files, <parentFile>$<number>

On a gridpane, call getChildren() to get list of children, can then edit.











