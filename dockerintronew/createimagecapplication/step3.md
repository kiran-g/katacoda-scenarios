Build the C application using Makfile

1. Create an empty Makefile
 
    `Makefile`{{open}} (Click here)
 
    Note: Makefile is a old unix method for build automation
    
2. Copy the following code into it:

<pre class="file" data-target="clipboard">
all:
&#09;gcc -o hello -static hello.c
</pre>

3. Now build the application:

    `make`{{execute}}

4. Test the application by running it in the host machine:

    `./hello`{{execute}}
