## introduction

Makefile is nothing but a set of rules to compile your files. they execute the rrules provided that the conditions are met, if any.

the general format of Makefile is  :

```
file: prerequisites
	commands to be executed
```

Makefiles make use of tabs for indentation and not spaces and will throw errors if used instead of tabs.

let us see a simple example:

```
foo:
	echo "foobar"
```

there are 2 ways to run the file. you can run it with just the ***make***, as there are no other files in it it will just run the first one by default.

the other way is with ***make foo***. here we are specifying what to run.

Makefile runs the echo command only if the foo file doesn't already exist. which may seem off. Then should one keep deleting a file after makinf changed to be able to run with make.

Nope. that is where the prerequisites come in hand. we'll go in depth later on but in brief with prerequisites it compares the timestamps of the 2 files and if the file has changed the timestamp does too and make run the command if the prerequisite is new than the file mentioned. we'll get back to that later. Let us tackle it one at a time.

run the Makefile in the present directory and observe the output.
for the later ones each Makefile would be put in their own directory to avoid confusion and will state which directory to run.


>Note: Makefiles need to named "Makefile" for the build system to recognize and execute it.
