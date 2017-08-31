# This week we learned, a whole lotta C.

## Some notes for the week in lecture.
In C, what does main do in

```c
#include <stdio.h>

int main(void)
{
    printf(""hello, world\n"");
}
```
*  `main` signifies the part of code that you want to run."

computers only operate in 1s and 0s, aka
*  binary

code written by humans that humans can read
*  source code

code that computers can understand
*  machine code

software that can translate code from source code to machine code.
*  a compiler

another name for the terminal
*  command line interface

GUI
*  graphical user interface, something that a user can click on to manipulate information and files on a computer

name what the command clang does
*  (The C language) , a command to tell the compiler to take my source code and compile the thing.

name what we call the default name for compiled programs in C
*  a.out

"give me an example of command line arguments"
*  ~/workspace/ $ clang -o hello hello.c

where -o is a flag that stands for output, so that when you enter hello, it will compile the file hello.c"

"in the terminal, what does
`ls` do?
*  provides a list of all files in the current directory"

"in the terminal, what does
`rm` do?
*  removes a file that you name such as
rm test.c"

define `cd`
*  a way to change into a directory

define `mkdir`
*  in a terminal, a way to make a new directory

define `rmdir`
*  in a terminal, a way to remove a directory.

"you see this code, what does this mean?

```c
   string name = get_string();
   printf(""hello, %s\n"", name);
```
*  you prompt the user to enter a name and store it in a variable named name.
   You then print out hello and the person's entry as a string substitution."

when you ask for an int, you get an
*  integer. Which are not real numbers. You have to ask for something different for the computer to work differently.

Define float
*  the data type you use to work with decimals


"Define overflow
*  when a number gets too big for the bits used for it.
   Computers can't handle too big of numbers as the space it has in RAM will run out if too big"

Define floating point imprecision
*  floats have a finite number of bits

"list the ways we can use string interpolation with these different data types?
*  You need to use
   %c, %f, %d, %i, %lld, %s"

bool
*  one of two values, either true or false

char
*  for a single character

double
*  for large real numbers, with more bits than a normal float

float
*  used for real numbers, decimals

int
*  integer

long long
*  used for large whole numbers w bits more than a normal int

string
*  characters marked by a quote

name the code you would use to show 55 decimal places in a string
*  `printf("%.55f\n", 1.0 / 10.0);`

name how you'd code a single character in C
*  You wrap a single characters in C with single quotes

"describe the syntax of a switch statement
*  //it looks like the following

```c
#include <cs50.h>
#include <stdio.h>

int main(void)
{
    char c = get_char();
    switch (c)
    {
        case 'Y':
        case 'y':
            printf(""yes\n"");
            break;
        case 'N':
        case 'n':
            printf(""no\n"");
            break;
        default:
            printf(""error\n"");
            break;
    }
}
```

Define a C prototype
*  A C prototype is the function signature. You need to add the signature before its use in a function as C programs are read from top to bottom.
   One line statements that define functions."

Define a library
*  a group of functions and prototypes, in a separate file, that you can use in your current file.


what makes for a good candidate to refactor code?
*  anytime you find yourself repeating code, you can refactor it.

"what does it look like to make your own function in C
*  Two examples, each have side effects of its execution.
// the main program, where it will do cough 3 times and sneeze 3 times.

```c
int main(void)
{
    cough(3);
    sneeze(3);
}

void cough(int n)
{
  say(""cough"", n);
}

void say(string word, int n)
{
 for (int i = 0; i < n; i++)
  {
    printf(""%s\n"", word);
  }
}

```

Define abstraction
*  building layers upon which others can work. Each layer can work together to form more complex layers.


preprocessing
*  lines in a program like #include, which tells our computer to look elsewhere for that file to make available for that program.


compiling
*  `clang -S hello.c`
where the computer takes your source code and translates it into something a machine can better understand."


assembling
*  where assembly code is translated from it to machine code.


linking
*  when the computer takes the code in machine language to create a final program.


given the command line
and I type ls
when I hit enter
*  then I see a list of all the files in my current directory.
   list, you can see all the files in your current directory"


given the command line
and I type cd
and the name of the directory
when I click enter
*  then I'm taken to that directory
   cd stands for change directory"


given the command line
define . (dot)
*  dot stands for the current directory
   ` ./`

given the command line
define .. (two dots)
*  two dots stands for the directory above.
../


given the command line
when I press ctrl + l (the letter L)
*  then I will clear the screen"


given the command line
when I press cd
*  then I'm taken to the home directory

given the command line
and I type in mkdir
and I give it a name
when I hit enter
*  then I've created a new directory


given the command line
and I type cp
and I enter <source> <destination> as two arguments
*  Then I've copied the file from one folder to another.


given the command line
When I want to copy a directory
*  Then I type cp -r <directory_name> <destination directory>
to recursively go through each file and copy"


given the command line
When I want to delete a file
*  Then I type rm -f <file>"


given the command line
When I want to delete a directory
*  Then I type rm -r <directory>"


given the command line
When I type rm <file>
*  Then I see a prompt that asks me, you sure you want to remove?"


given the command line
And I want to remove the files and the folders within a file
*  Then I can combine flags
And I'd type
rm -rf <directory>"


given the command line
When I want to move a file
*  Then I can move the file one from another.
And I'd type
mv  <old destination/file> <new destination/file>"


int
*  takes up 4 bytes of memory, can only take up 32 bits of memory.
from -2^21, to 2^31-1"


unsigned int
*  unsigned means a qualifier, doubles the range for a positive values, but disallows negatives


name how to control the number of decimal places in a float when printing out the float to a string.
*  use string interpolation

```c
float f;
...
printf(""2 Decimal places %.2f"", f);
```



when you want to validate a user's information on a prompt, then you can use a
*  do while loop, as it will execute at least once, then will keep looping until you give a condition to break the loop.

```c
int i;
do {
  printf(""Number greater than 5: "");
  i = get_int;
} while (i < 5 );
```


## I submitted problem set 1

```c
// hello.c
#include <stdio.h>

int main(void)
{
    printf("Hello, world!\n");    
}
```

```c
// water.c
#include <stdio.h>
#include <cs50.h>


/* include the */

int main (void)
{
    printf("Minutes: ");
    int minutes = get_int();

    printf("Bottles: %i\n", minutes * 12);
}

```

```c
// mario, less comfortable
#include <cs50.h>
#include <stdio.h>

void print_hash_space( string hash_space , int n);


int main(void)
{
    int n;
    do
    {
        printf("Height: ");
        n = get_int();
    }
    while (n > 5 || n < 0);

    if ( n > 0 && n < 6)
    {
        int space_count = (n - 1);
        for (int j = 0; j < n; j++)
        {
            int brick_count = (j + 2);
            print_hash_space(" ", space_count);
            print_hash_space("#", brick_count);
            printf("\n");
            space_count--;
        }        
    }
}

// set either " " or "#" and a number, prints that
void print_hash_space( string hash_space , int n )
{
    for(int i = 0; i < n; i++)
    {
        printf("%s", hash_space);
    }
}
```

```c
// greedy.c
#include <cs50.h>
#include <stdio.h>
#include <math.h>

void print_coins( int change, int original_amt );

int main(void)
{
    float f;
    do
    {
        printf ( "O hai! How much change is owed?\n" );
        f = get_float();    
    }
    while ( f < 0 );

    int n = f;
    int change = round( ( f - n ) * 100 );
    print_coins( change, n );

}

// function used to calculate the number of coins to return, given an amount of money in decimals.
void print_coins( int change, int original_amt )
{
    int coins = 0;
    if ( change == 0 )
    {
        printf( "%i\n", original_amt );    
    }
    else
    {
        while ( change >= 25 )
            {
                coins++;
                change-= 25;
            }
            while ( change >= 10 )
            {
                coins++;
                change-= 10;
            }
            while ( change >= 5 )
            {
                coins++;
                change-= 5;
            }
            while ( change >= 1 )
            {
                coins++;
                change-=1;
            }
        printf("%i \n", coins);
    }
}

```
