# REFLECTION QUICK REFERENCE

# Getting Class class instances

## Get a Class class from string name of class

	Class c = Class.forName("class-name");

## Get a Class class from existing obj

	Class<?> c = obj.getClass();

# Fields

### Gets all fields in class, including those inherited

	Field[] fields = c.getFields();

### Gets all fields declared in class, EXCLUDING inherited fields.

	Field[] fields = c.getDeclaredFields();

	field.getName(); 
SET
	field.set(obj, value); //throws check exception
	// this will throw exeptions if private or final as well
	// to avoid this, call:

 	field.setAccessible(boolean);

# Methods

### Gets all methods in class, incl. inherited

	Method[] methods = c.getMethods();	
	
### Gets all methods in class, EXCLUDING inherited
	
	Method[] methods = c.getDeclaredMethods();

## Invocations
	
	method.invoke(obj, Args <...>);
	// watch for private/static exceptions as with fields
	// to call static method:
	
	method.invoke(null, Args <...>);

	// to access private methods:

	method.setAccessible(boolean);

	
# Annotations
### returns if given annotation is present on class

	class.isAnnotationPresent(<annotation-name>.class);
	
### see if method has annotation

	method.isAnnotationPresent(<annotation-name>.class);

### get annotation

	<an-name> an = method.getAnnotation(<an-name>.class);
	// get params, if any, by:
	an.paramName();












