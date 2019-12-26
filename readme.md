# Java/Maven Project Skeleton for JDT
This is a sample project to be used with editors/IDEs to create a new java
project from scratch, like a maven-archetype. This project is useful to be used
as a base when using an editor that uses the Eclipse JDT as its language server.

## What it does
This project has the necessary files to code in Java using Visual Studio Code or
SpaceVim (and probably anything else that uses JDT in the backend), including
the eclipse-specific files that those editors won't create for you.

## Using with VS Code
1 - Have Visual Studio Code installed.

2 - Install the Java Extension Pack at the extensions side panel.

3 - Clone this repository somewhere in your machine.

4 - Delete the .git folder in this cloned project.

5 - Go to VS Code and select File -> Open Folder and select the folder with the cloned project.

6 - Change the file .project to reflect your project name.

7 - Delete all files named deleteme.txt.

8 - Change the pom.xml to reflect your project information.

9 - You'll probably want to add the following to your .gitignore:

    ```
    .classpath
    .settings
    .project
    ```

10 - Enjoy. :)

## How well it works?
With this project setup, I found everything I needed from Eclipse inside Visual
Studio Code. The extension simply works fine.

At the Java Extension documentation, it is mentioned that Gradle is not
supported yet. The project I was working on when I came up with this solution
was a Maven project, so I haven't tested with Gradle. It works fine with Maven.

You need to take a look at the documents to see where things are, but everything
is there (just at other places).

## Why?
I am a long-time Eclipse user, but even knowing that it is among the best IDEs
for java around there, we have to recognize that while it brings a lot in terms
of functionality, it has stopped in time when talking about UX and usability.
This is noticeable mainly when using a modern code editor like VS Code.

Also, after not getting to *import a project from GitHub as a Maven Project and
having all the source folders being recognized properly* in a timely manner
because of extensions that would not install and other seemingly unecessary
steps for a simple project import, I decided it was time to look somewhere else.
Even NetBeans did that without problems.

Even though, historically speaking, using a non-dedicated Java IDE like Eclipse,
NetBeans or Idea is pretty much an exercise in frustration. Not having simple 
things like auto-imports, refactor and getter/setter code generation when coding
in Java is plain masochism. Using an editor without those features is a no-go.

Some people had the smart idea of using the Eclipse JDT as a language server, 
what pretty much allows you to use the good things of Eclipse (the backend) with
a better front-end. BUT, in the both cases I tried (VS Code and SpaceVim), it
wouldn't work at all. After some research, I learned that even though everything
I wanted was a simple Maven project imported, the JDT *needs* files like the
**.classpath** and **.settings** created in your project folder for the editor
features to work properly.

Having to use Eclipse just to create the project and setup the classpath using
the UI sounds idiot in my opinion as I'm trying to *not* use Eclipse, right?
Also, no one wants to memorize the classpath XML schema to rewrite it every time
we create a new project, even because for simple projects it should always be
the same.

Well, for that reason I created that project skeleton that have the eclipse
files created and setup, along with a standard pom.xml and the necessary
folders to get the project up and running with a single checkout.

*I still had to go through the idiot eclipse process once to get this done.*