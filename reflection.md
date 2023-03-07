#======== REFLECTION QUICK REFERENCE ========

#Getting Class class instances

##Get a Class class from string name of class

	Class c = Class.forName("class-name");

##Get a Class class from existing obj

	Class<?> c = obj.getClass();

#Fields

###Gets all fields in class, including those inherited

	Field[] fields = c.getFields();

###Gets all fields declared in class, EXCLUDING inherited fields.

	Field[] fields = c.getDeclaredFields();

	field.getName(); 
SET
	field.set(obj, value); //throws check exception
	// this will throw exeptions if private or final as well
	// to avoid this, call:

 	field.setAccessible(boolean);

#Methods

	
	
