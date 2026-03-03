```
try with finally only allowed
try with catch only allowed
try alone -> not allowed


try {
    // A
} catch (Exception e) {
    // B
} finally {
    // C
}

No exception	        : A → C
Exception caught	    : A → B → C
Exception not caught	: A → C → crash
return in try	       : try → finally → return
return in catch	     : catch → finally → return

try has system.exit(0) -> finally doesnt execute
try has return -> cache return value, run finally, then return
both try and finally have return -> value returned by finally 

MULTIPLE CATCH : 

catch (E1 | E2 e) -> E1 and E2 should be disjoint

catch(E1 e){}
catch(E2 e){}
E1 should not be parent of E2

TRY WITH :

FileInputStream fis = new FileInputStream("file.txt");
      // AutoCloseable implemented
try {
    // use fis
} finally {
    fis.close();
}

===

try (FileInputStream fis = new FileInputStream("file.txt")) {
    // use fis
}


Throwable
 ├── Error                  (JVM problems, don’t catch)
 └── Exception
       ├── RuntimeException  ← Unchecked
       └── Other Exceptions  ← Checked
       
Checked exception : Force developers to acknowledge recoverable problems.
Checked = External / Recoverable problems - File system/Database/Network/I-O

Unchecked = Programming bugs (runtime) eg. 

Rule : 
handle (using try-catch) / throw-up checked exception else get COMPILE ERROR
runtime error need not be try-catched / thrown-up. It will compile fine.

good practice : dont catch runtime exception, these are bugs not recovereable conditions


class InvalidUserInputException extends Exception  // Checked
class InvalidStateException extends RuntimeException  // Unchecked





API design good practice :
try {
    file.read();
} catch (IOException e) {
    throw new RuntimeException(e);
}
```
