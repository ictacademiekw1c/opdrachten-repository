####[kleurcode]rgba(255,192,0,1)

#HOOFDSTUK13
In hoofdstuk 13 worden de volgende C++ structuren geïntroduceerd:

- Selecties en herhalingen
- Relationele operatoren
- Logische operatoren

##Selecties en herhalingen

### Syntax if-statement

**IF ELSE**

if-else-statement
Syntax:

* if (*expression*)
   *statement*;
   [else
   	*statement*];

**IF-EXISTS**

if-exists-statement

Syntax:

*  __if_exists (*identifier*)
         {
               *statement*;
         };

**IF-NOT-EXISTS**

if-not-exists-statement.

Syntax:

* __if_not_exists (*identifier*)
         {
               *statement*;
         };

###Syntax switch-statement
switch-statement.
Syntax:
	switch (*expression*)
	case *constant-expression*:
	{
		*statement*;
		break;
	}

###Syntax for-statement

for-statement.

Syntax:

​	for (init-expression; cond-expression; loop-expression)

​	{
​		 statement;

​	}

###Syntax while-statement

while-statement.

Syntax:

·         while (*expression*)
       {
             *statement*;
       }

###Syntax do-while-statement

do-while-statement.

Syntax:

·         do
       {
             *statement*;
       }
 while (*expression*);

###Syntax break-statement

break-statement.

Syntax:

​	break;

###Syntax continue-statement

continue-statement.

Syntax:

​	continue;

###Syntax goto-statement

goto-statement.

Syntax:

​	goto *identifier*;

...

​	*identifier*: *statement*;

###Syntax null-statement

null-statement.

Syntax:

​	;

###Syntax return-statement

return-statement.

Syntax:

​	return *[*(*expression*)*]*;

##Relationele operatoren

###Is ongelijk aan

!=

Syntax:

​	*operand* != *operand*

###Is gelijk aan

==

Syntax:

​	*operand* == *operand*

###Is kleiner dan

< 

Syntax:

​	*operand* < *operand*

###Is groter dan

\> 

Syntax:

​	*operand* > *operand*

###Is kleiner dan of gelijk aan

<=

Syntax:

​	*operand* <= *operand*

###Is groter dan of gelijk aan

\>=

Syntax:

​	*operand* >= *operand*

##Logische operatoren

###En

&&

Syntax:

​	*operand* && *operand*

###Of

||

Syntax:

​	*operand* || *operand*

###Niet

!

Syntax:

​	! *operand*