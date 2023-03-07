# ANNOTATIONS

An annotation is like "metadata" for the code, so to speak
EG @Override is used to ensure you're properly overriding a method
EG @SuppressWarnings("warning-name")

Annotations can be added to almost any code

## Creating custom annotations

### Creating class annotation

	//to create @ClassAnnotation
	
	public @interface ClassAnnotation {
	
	}

	// To enforce type:
	
	@Target(Args)
	// args are ElementType.xxx
	// EG ElementType.TYPE 
	//    ElementType.METHOD
	// For a list, use inline Array decl: {a, b, c}
	
	// To specify retention
	
	@Retention(RetentionPolicy.xxx)
	// options: SOURCE, CLASS, RUNTIME

	
