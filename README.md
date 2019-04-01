LAMP Configuration Using Source Code


The LAMP stack is the foundation for Linux hosted websites is the Linux, Apache, MySQL and PHP (LAMP) software stack.

The Four Layers of a LAMP Stack
Linux based web servers consist of four software components. These components, arranged in layers supporting one another, make up the software stack. Websites and Web Applications run on top of this underlying stack. The common software components that make up a traditional LAMP stack are:


•	Linux: The operating system (OS) makes up our first layer. Linux sets the foundation for the stack model. All other layers run on top of this layer.


•	Apache: The second layer consists of web server software, typically Apache Web Server. This layer resides on top of the Linux layer. Web servers are responsible for translating from web browsers to their correct website.


•	MySQL: Our third layer is where databases live. MySQL stores details that can be queried by scripting to construct a website. MySQL usually sits on top of the Linux layer alongside Apache/layer 2. In high end configurations, MySQL can be off loaded to a separate host server.


•	PHP: Sitting on top of them all is our fourth and final layer. The scripting layer consists of PHP and/or other similar web programming languages. Websites and Web Applications run within this layer.
We can visualize the LAMP stack like so:
 


There are three distinct steps in this process:

1.	Configure the software
The configure script is responsible for getting ready to build the software on your specific system. It makes sure all of the dependencies for the rest of the build and install process are available, and finds out whatever it needs to know to use those dependencies.
UNIX programs are often written in C, so we’ll usually need a C compiler to build them. In these cases the configure script will establish that your system does indeed have a C compiler, and find out what it’s called and where to find it.

    In some cases you need to run ./BUILD/autorun.sh script to get configure file.


2.	Build the software
Once configure has done its job, we can invoke make to build the software. This runs a series of tasks defined in a Makefile to build the finished program from its source code.
The tarball you download usually doesn’t include a finished Makefile. Instead it comes with a template called Makefile.in and the configure script produces a customized Makefile specific to your system.


3.	Install the software
Now that the software is built and ready to run, the files can be copied to their final destinations. The make install command will copy the built program, and its libraries and documentation, to the correct locations.
This usually means that the program’s binary will be copied to a directory on your PATH, the program’s manual page will be copied to a directory on your MAN PATH, and any other files it depends on will be safely stored in the appropriate place.
Since the install step is also defined in the Makefile, where the software is installed can change based on options passed to the configure script, or things the configure script discovered about your system.
Depending on where the software is being installed, you might need escalated permissions for this step so you can copy files to system directories. Using sudo will often do the trick.


LOCAL INFRASTRUCTURE USED

MACHINE: DELL Inspiron 14   Laptop

CONFIG:  Core I3 2.00GHZ CPU, 4GB RAM, 1TB HDD

OS:  REDHAT Linux el7.0, Kernel = 3.10

Apache = Httpd 2.4

Mariadb = Mariadb 10.2.22

PHP = php 5.5


 Source code installation Steps

1   ./configure

2   make

3   make install     

