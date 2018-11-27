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

Will it work? What will happen?

1. Try to use Select-Object to make the above command work.

## Lesson 7 - Variables

1. Store todays date in a variable called $Date

1. Write the day of the month to screen

1. Investigate $Date and see if you can find a method to modify the date.

1. See if you can putput the date of the last day in the previous month.

## Lesson 8 - Working with strings

1. Create a variable called $Name and store you name in it.

1. Create another variable called $Day and store todays day in it.

1. Create third variable valled $Greeting containing a greeting to the name in $Name and saying wich day it is today. Example output:
  Hello Simon, today is tuesday.

1. Create a new variable called $NewName that contains a new name.

1. Replace the name in $Greeting with the new name.

## Lesson 9 - Logic flow

1. Save the service W32Time in a variable

1. If the service is running, write a positive message to screen

1. If the service is not running, write a warning to screen

1. Write a script that saves the strings 'Alfa', 'Bravo' and 'Charlie' in a variable

1. Use a switch statement to write a message that tells which letter each name starts with

## Lesson 10 - WMI

1. Get the serial number of your computer and save the last 8 characters in a string called $Serial

1. Using the class Win32_SystemEnclosure to find and store your computers chassis types.

1. If the chassis type are 9, 10, 11 or 14 set the variable $Type to 'L'

1. If the chassis type are 8, set the $Type to 'T'

1. If the cassis type are anything else than 8,9,10,11 or 14, set $Type to 'W'

1. Combine $Type with a dash (-) and $Serial to create a computername and stor that in $Name

## Lesson 11 - PowerShell Remoting

Todo...

## Lesson 12 - Version Control

Todo...

## Lesson 13 - PowerShell Tools

Todo...

## Lesson 14 - Creating parameters





