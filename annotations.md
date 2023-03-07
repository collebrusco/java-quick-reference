# ANNOTATIONS

An annotation is like "metadata" for the code, so to speak
EG @Override is used to ensure you're properly overriding a method
EG @SuppressWarnings("warning-name")

Annotations can be added to almost any code
To access these, see reflection.md

## Creating custom annotations

### Creating class annotation

	to create Annotation:
	
	public @interface Annotation {
	
	}

	To enforce type:
	
	@Target(Args)
	// args are ElementType.xxx
	// EG ElementType.TYPE 
	//    ElementType.METHOD
	// For a list, use inline Array decl: {a, b, c}
	
	To specify retention:
	Retention refers to how long java will remember that an annotation exists.
	Whether it's only needed during compilation, still needed in bytecode, or also at runtime
	@Retention(RetentionPolicy.xxx)
	// options: SOURCE, CLASS, RUNTIME

	To add param:
	
	public @interface Annotation {
		int integerParam() default 1;
	}
	
	Note that they're declared as if they're methods
	default is optional

	To pass them:

	@Annotation(integerParam = 6)

	
