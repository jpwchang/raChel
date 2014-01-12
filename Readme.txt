The raChel programming language

This is a set of macros for C++ allowing users to program with Rachelism-like source code.
An example program written in raChel (example.cpp) is included.
To write your own programs in raChel, simply include the following line at the top of your code:
#include "Rachel.h"
(Your source file will have to be in the same directory as Rachel.h)
Note that this language depends on the auto keyword, introduced with C++ 11
Therefore, you will need a C++ 11 compatible compiler to use raChel.
C++ 11 is supported by Visual Studio 2013 and up and gcc 4.7 and up.

LANGUAGE FEATURES
------------------
Being just a set of macros for C++, raChel supports all C++ features; it just uses some different syntax.
The syntax changes are as follows:
-Like in C++, you need a main function. You declare a main function as follows:
	LET_ME_TELL_YOU A_STORY
	SO
		<code goes here>
	THE_END
	-note the space between YOU and A
-For general use, WATCH_OUT represents an open brace ({) and ANYWAY represents a closing brace (})
-To create a new variable, use THIS_KID <variable name> WAS <initial value>
	-e.x. THIS_KID zoab WAS 10; makes a variable called zoab with the value 10
	-Since THIS_KID masks the auto keyword, you MUST give initial values to variables
	-THIS_KID should work for any primitive type since it uses auto
	-Modifying variables works just like in C++: <variable name> WAS <initial value>
-While loops can be made with the following syntax: DO_YOU_BUY <conditions> BRO
	-e.x. DO_YOU_BUY i > 10 BRO will run as long as i is greater than 10
-For loops use the following syntax: 
	I_FEEL_LIKE THAT_KID <name> WAS <initial value> AND_MAYBE <condition> AND_MAYBE <action> THEN
	-note this only works for integer type indexing variables
	-Common actions include:
		-GREW_UP (increment), e.x. zoab GREW_UP
		-I_HAVE_SOME_BAD_NEWS_FOR (decrement), e.x. I_HAVE_SOME_BAD_NEWS_FOR zoab
-The basic structure of an if/else if/else block is:
	IF <condition> THEN
		<code goes here>
	BUT_ACTUALLY_THOUGH IF <other condition> THEN
		<code goes here>
	BUT_ACTUALLY_THOUGH
		<code goes here>
-To print stuff, use THEYRE_LIKE
	-e.x. THEYRE_LIKE "Hello World"
	-You can optionally add a newline character with MAN, e.x. THEYRE_LIKE "Hello World" MAN;

For more guidance, see the example file