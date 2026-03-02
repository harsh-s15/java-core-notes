
```
abstract in java : incomplete things
meant to be extended / implemented

abstract class : may / may not have abstract methods
abstract method : must be inside abstract class

abstract methods cannot be implemented

final + abstract : illegal combination

abstract class Animal {


    public String name;
    Animal(String name){
        this.name = name;
    }
    
    void breathe(){
        sout("breathing");  
    }       

    abstract void greet();         // cannot have body, subclasses must implement it to become non-abstract
    void setName(String name){
        this.name = name;
    }
}



public class Dog extends Animal{

    Dog(String name) {         // if no-arg constructor absent in parent, child must have a constructor calling super
        super(name);
    }

    @Override
    void greet() {
        System.out.println(name+" bhow");
    }
}
```
