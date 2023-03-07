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
