# Windows-basic-commands-batchscript
Ex08-Windows-basic-commands-batchscript

# AIM:
To execute Windows basic commands and batch scripting

# DESIGN STEPS:

### Step 1:

Navigate to any Windows environment installed on the system or installed inside a virtual environment like virtual box/vmware 

### Step 2:

Write the Windows commands / batch file . Save each script in a file with a .bat extension. Ensure you have the necessary permissions to perform the operations. Adapt paths as needed based on your system configuration.
### Step 3:

Execute the necessary commands/batch file for the desired output. 




# WINDOWS COMMANDS:
## Exercise 1: Basic Directory and File Operations
Create a directory named "my-folder"

## COMMAND AND OUTPUT
![Screenshot 2025-05-18 222923](https://github.com/user-attachments/assets/a1e0f62f-105b-42ee-90a2-34462f261bdb)

Remove the directory "my-folder"

## COMMAND AND OUTPUT
![Screenshot 2025-05-18 223555](https://github.com/user-attachments/assets/bdde954a-a317-494a-ad6a-35f3e9da6b4e)


Create the file Rose.txt

## COMMAND AND OUTPUT

![Screenshot 2025-05-18 223828](https://github.com/user-attachments/assets/37effecd-f19d-481c-b5af-4e19dd173834)


Create the file hello.txt using echo and redirection

## COMMAND AND OUTPUT

![Screenshot 2025-05-18 223932](https://github.com/user-attachments/assets/064c7bb6-6092-40ef-aebc-d52e48c19abe)

Copy the file hello.txt into the file hello1.txt

## COMMAND AND OUTPUT

![Screenshot 2025-05-18 224337](https://github.com/user-attachments/assets/390f7085-5d43-4ade-b2d4-c6c8f70df305)

Remove the file hello1.txt

## COMMAND AND OUTPUT

![image](https://github.com/user-attachments/assets/27f5f7a8-ae9a-4adf-ac9d-975f869429ec)


List out the file hello1.txt in the current directory

## COMMAND AND OUTPUT

![image](https://github.com/user-attachments/assets/c5aaf312-d544-415c-9530-a1c992e42201)


List out all the associated file extensions 

## COMMAND AND OUTPUT

![image](https://github.com/user-attachments/assets/2351b9eb-9f55-4d36-994b-1011e92c7bfb)


Compare the file hello.txt and rose.txt

## COMMAND AND OUTPUT


![image](https://github.com/user-attachments/assets/dbd7ad68-a4ca-472a-922d-b5b5a7ff75a0)


## Exercise 2: Advanced Batch Scripting
1.Create a batch file named on the desktop. The batch file need to have a variable assigned with a desired name for ex. name="Jobhn" and display as "Hello, John".
```
@echo off
set name=John
echo Hello, %name%
pause
```

## OUTPUT

![Screenshot 2025-05-18 230242](https://github.com/user-attachments/assets/b8bfdd34-0930-46c2-b6ef-93cc99f0b9a5)



2.Create a batch file  on the desktop that checks whether a user-input number is odd or not. The script should:
Prompt the user to enter a number.
Calculate the remainder when the number is divided by 2.
Display whether the number is odd or not.
Ask the user if they want to check another number.
Repeat the process if the user enters Y, and exit with a thank-you message if the user enters N.
Handle invalid inputs for the continuation prompt (Y/N) gracefully.

```
@echo off
:loop
set /p num=Enter a number: 
set /a rem=%num% %% 2

if %rem%==0 (
    echo %num% is Even
) else (
    echo %num% is Odd
)

:ask
set /p ans=Do you want to check another number? (Y/N): 
if /I "%ans%"=="Y" goto loop
if /I "%ans%"=="N" goto end
echo Invalid input. Please enter Y or N.
goto ask

:end
echo Thank you!
pause
```


## OUTPUT

![Screenshot 2025-05-18 230804](https://github.com/user-attachments/assets/9521fed0-b5eb-4773-bab3-230afc089a8f)




3.Write a batch file that uses a FOR loop to iterate over a sequence of numbers (1 to 5) and displays each number with the label Number:. The output should pause at the end.
```
@echo off
for /L %%i in (1,1,5) do (
    echo Number: %%i
)
pause

```

## OUTPUT

![Screenshot 2025-05-18 231059](https://github.com/user-attachments/assets/149f7b18-9007-4a2e-91c3-1de5407aa537)



4.Write a batch script to check whether a file named sample.txt exists in the current directory. If the file exists, display the message sample.txt exists. Otherwise, display sample.txt does not exist. Pause the script at the end to view the result.

Instructions:
Use the IF EXIST conditional statement.
Make sure the script works for files located in the same directory as the batch file.
Use pause to keep the command window open after displaying the message.
Expected Output (if the file exists):

```
@echo off
if exist sample.txt (
    echo sample.txt exists.
) else (
    echo sample.txt does not exist.
)
pause
```

## OUTPUT

![image](https://github.com/user-attachments/assets/53a52591-1292-4b6e-8ad9-7a69d6c10e73)


5.Write a batch script that displays a simple menu with three options:
Say Hello – Displays the message Hello, World!
Create a File – Creates a file named newfile.txt with the content This is a new file
Exit – Exits the script with a goodbye message
The script should repeatedly display the menu until the user chooses to exit. Use goto statements to handle menu navigation.
```@echo off
:menu
cls
echo 1. Say Hello
echo 2. Create a File
echo 3. Exit
set /p choice=Choose an option (1-3): 

if "%choice%"=="1" goto hello
if "%choice%"=="2" goto create
if "%choice%"=="3" goto exit
echo Invalid choice.
pause
goto menu

:hello
echo Hello, World!
pause
goto menu

:create
echo This is a new file > newfile.txt
echo File newfile.txt created.
pause
goto menu

:exit
echo Goodbye!
pause
exit
```

## OUTPUT

![Screenshot 2025-05-18 234139](https://github.com/user-attachments/assets/2bf2f179-7b8f-4815-98e7-7221b1b6ad75)


![Screenshot 2025-05-18 234205](https://github.com/user-attachments/assets/e2d7713f-8753-4336-a380-135c05e12403)

![Screenshot 2025-05-18 234245](https://github.com/user-attachments/assets/b5fe8b8d-70ee-4c57-95c4-17d40a4b23c9)


# RESULT:
The commands/batch files are executed successfully.

