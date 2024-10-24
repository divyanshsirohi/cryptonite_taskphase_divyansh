Cyrptonite task 2


1.  Shell variables-

	we can print out variable names using ‘echo’ and prepending the variables with $

	variable can be assigned to any value using the ‘=’ operator but no spaces should be left around the equals to sign else it wont assign the value         correctly

	for a multi word variable assignment we can simple put “” around the value we want to assign it to

	variables are by nature local to the shell proccess they are initialised in but we can exporet them and make them global that enables them to be used by  any other shell

	the env command can be used to look at every exported variable

	using command substitution we can assign the value of a variable to the output of a command eg:- FLAG=$(cat /flag)

    using the ‘read’ command we can read a value and store it into a variable
    
    
2. Processes and jobs 

    ps - process status or process snapshot
    
    there are two systems of postfixes after ps
    
    i) standard system -
        -e list every process
        -f full format output
        -ef combines both
        
    ii) BSD system- 
    
        a - list process for all users
        x - list process not running in terminal
        u - user readable output
        
        aux - combines all
        
        -ef & aux 
        
        common: user PID TTY STIME CPUTime Command 
        
        unique:
        
            -ef: PPID(Parent process ID)
            aux: CPU & Memory % used by the process 
            
        in order to get rid of a certain process we can use teh kill command with PID of the command in order to  terminate it
        
        instead of kill we can also use the crtl-c shortcut to end any process going on in the terminal
        
        or we can use ctrl-z to suspend the process
        
        after suspending a certain program we can once again resume it using the 'fg' command.
        
        we can use the 'bg' commmand to keep the commadn running in the backround
        
        if we append '&' to a program we dont need to suspend the program then run it in the background from the start  
        
3. Perceiving Permissions: 

    we can use chmod to assign permissions
    
    eg:- 
    chmod u+x filename will give permission to the root user to execute the file
    
    chmod u-x will give permission to the root user to be now unable to execute the file
    
    we can also use the = operator instead of the + or - to set the permissions without adding or removing just one or few
    
    
4. Untangling users

    su - switch user
    
    we can su into other users and use the permissions assigned to them
    
    sudo - super user do
    
    there is a list of sudoers and if we belong to that we can use sudo as a prefix before commands and execute and program as per our wish
    
5. Chaining commands 

    we can use ; to chain multiple commands into one line in the terminal
    
    instead of using ; we can create a script which is in the '.sh ' format
    
    this script file can be run using bash command
    
6. pondering PATH

    
    PATH is an environmental variable in Linux and other Unix-like operating systems that tells the shell which directories to search for executable files (i.e., ready-to-run programs) in response to commands issued by a user. It increases both the convenience and the safety of such operating systems and is widely considered to be the single most important environmental variable.
    
    A user's PATH consists of a series of colon-separated absolute paths that are stored in plain text files.

   The PATH basically tells the terminal where the user is located. it makes it ewasier for us to use the command we use in our terminals on a daily basis.

   

    
        
        
        
