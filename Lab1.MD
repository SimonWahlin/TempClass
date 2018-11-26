# Module 1

## Lesson 2 - Safety and Security

### Exercise 2.1 - Execution Policy

1. Open PowerShell as administrator and run:

```PowerShell
Get-ExecutionPolicy -List
```

This will display a list of scopes and the execution policy set in each scope.

Use Set-ExecutionPolicy to set the exectuon policy to RemoteSigned if that is not already set.

### Exercise 2.2 - Transcript logging

1. To save a log of everything you do in a PowerShell session, use the command Start-Transcript. Open PowerShell and run the following code:

    ```PowerShell
    Start-Transcript -Path "~\Documents\PowerShellCourse.txt" -IncludeInvocationHeader -Append
    ```

    This will create a transcript file in your documents folder.

1. Locate the file and open it in your favourite text-editor.

    ```Text
    TIP: Use a text-editor automatically reloads the file when it has changed on disk. That way you don't need to reopen the file over and over again.
    ```

1. Run a few commands in the PowerShell console and look at the contents of your transcript after each command.

    ```PowerShell
    Get-Command -Name Get-Service
    dir
    ```

1. Stop the transcript session with the command Stop-Transcript.

    ```PowerSHell
    Stop-Transcript
    ```

## Lesson 3 - Getting started

### Exercise 3.1

Use Get-Command to find a command to create an SMB share.

## Lesson 4 - HELP

### Exercise 4.1

1. Use the help system to get the full help for Get-Command

1. Which parameter can be used to quickly see how a cmdlet can be run?

1. How can I list all commands that have a parameter called UserName?

1. How do I get information about only the parameter ParameterType for Get-Command?

1. What is the parameter ParameterType used for with Get-Command?

## Lesson 5 - Output and pipeline

### Working with dates
1. Find a command that will return the current date.

1. Run the command and see if you can find which day of the year it is today

1. Use select-object to only display the day of the year

### Filtering, selecting and sorting
1. Find a command that will list all services on your machine

1. Filter the output to only show services running

1. Measure the number of objects to see how many services are running

1. Group all services by their status to see how many are running vs stopped.

1. Use Get-ChildItem to list files in your current folder

1. List the files in order of last modified.

1. List files in order of size

1. List only the 4 largests files.

1. List the full path of the 4 largest files.

## Lesson 6 - Pipeline bindings

1. Run the command:

```PowerShell
get-service -name w32Time | get-process
```

It runs, but we get an error, why is that? What is get-process trying to do?

1. Look at the command without running it:

```PowerShell
Get-Process -Id $PID | Get-Item
```

Will it run? What will happen?

1. Try to run the comand above. What happens?

1. Look at the command without running it:

```PowerShell
Get-Process -Id $PID | Get-Item | Get-Process
```
