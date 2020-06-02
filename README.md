# Introduction-to-system-calls

Includes :
1. a program in C which emulates the behaviour of Linux cat command.
2. Implementation of a mini shell of my own. The shell

  a. When run, displays a coool prompt of your choosing and prompt the user for input.
  
  b. When given a command with arguments, it creates a child process and run the command with its arguments. By default it  wait for the 
    command to finish before displaying the prompt again.     
    
  c. If only one command is typed followed by &, it runs the command in back ground and displays the prompt immediately. Hush imitate
     the  same behaviour.
     
  d. When given a command followed by a redirection operator (>, >>) followed by a filelename, it redirects the output of the command to 
     the said file by overwriting or appending to it respectively.
     
  e. It keeps track of the names and PIDs of the commands it has launched that are still running. It implements a command myps which 
     should list all the names and PIDs of the commands that haven't finished yet.
     
  f. Moreover, the shell would:   
  
        + modify its PATH variable to add the current directory to its list of paths. This way
        one won't have to type the leading dot-slash (./) when running our executables.
        
        + have a command mylsenv it lists all its environment variables and
        their values.
        
        + when typed a string VAR=xxxx on the command prompt, it adds the variable
        VAR to its list of environment variables assigning it the value xxxx. If the variable
        exists already, it overwrites its old value with xxxx. A command
        show VAR displays the value of the variable VAR.
        
  g. It have implementation of built-in commands cd and pwd which updates and prints the current working directory respectively.
  
  h. It exits if the user types exit at the prompt. It checks if there are any child processes still running and kill them  
     before exiting.
     
