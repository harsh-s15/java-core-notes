```
bytecode : platform independent intermediate code (.class)
main.java -> main.class (done by javac)

JVM : java virtual machine
sandbox
loads class
executes code (line by line)

JRE : java runtime environment
JRE = JVM + Libraries

bytecode - jvm understands
machine code - cpu understands

interpreter loop (part of jvm) : executes bytecode directly (may be a cpp loop maps instructions to 
native operations)
JIT : converts hot code into machine code for speed


====================================
JDK superset of JRE superset of JVM
====================================

JVM is platform dependent, windows jvm != Linux jvm
but both run same bytecode
jvm is the execution engine


JRE : everything needed to run java programs
jre = jvm + standard libs (java.lang, java.utils...)


JDK : everything needed to run + develop java programs
jdk = jre + tools
tools = javac, jdb, jar,...


each thread has its own stack
```
