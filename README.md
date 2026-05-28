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
<img width="779" height="236" alt="image" src="https://github.com/user-attachments/assets/1f3e53f3-88c6-4c75-bc22-97e1c89be0bc" />

Remove the directory "my-folder"

## COMMAND AND OUTPUT
<img width="428" height="31" alt="image" src="https://github.com/user-attachments/assets/6e0b48d5-1335-4a17-a944-0bb294ecd9c0" />


Create the file Rose.txt

## COMMAND AND OUTPUT
<img width="753" height="255" alt="image" src="https://github.com/user-attachments/assets/19d42ffc-3add-4598-8c78-6a05d0a027f9" />


Create the file hello.txt using echo and redirection

## COMMAND AND OUTPUT
<img width="606" height="49" alt="image" src="https://github.com/user-attachments/assets/3f6f8f6f-ed86-4669-bb47-12039f977446" />

Copy the file hello.txt into the file hello1.txt

## COMMAND AND OUTPUT
<img width="606" height="49" alt="image" src="https://github.com/user-attachments/assets/d3e3c196-405c-47ec-93a1-6750ed64de0f" />

Remove the file hello1.txt

## COMMAND AND OUTPUT
<img width="506" height="30" alt="image" src="https://github.com/user-attachments/assets/ff961cc8-c721-4784-ab00-42d4734a0312" />

List out the file hello1.txt in the current directory

## COMMAND AND OUTPUT
<img width="594" height="169" alt="image" src="https://github.com/user-attachments/assets/57e6653d-279f-427c-bc55-aa444652c633" />

List out all the associated file extensions 

## COMMAND AND OUTPUT
<img width="497" height="500" alt="image" src="https://github.com/user-attachments/assets/80ddf0b8-eddc-442e-94eb-f7454e913456" />


Compare the file hello.txt and rose.txt

## COMMAND AND OUTPUT
<img width="524" height="547" alt="image" src="https://github.com/user-attachments/assets/7218baa3-dcff-4d27-b0f5-5d070ef40e64" />

## Exercise 2: Advanced Batch Scripting
Create a batch file named on the desktop. The batch file need to have a variable assigned with a desired name for ex. name="John" and display as "Hello, John".





## OUTPUT

<img width="477" height="86" alt="image" src="https://github.com/user-attachments/assets/ef96886e-c005-4882-a7b2-b7910def9aa3" />


Create a batch file  on the desktop that checks whether a user-input number is odd or not. The script should:
Prompt the user to enter a number.
Calculate the remainder when the number is divided by 2.
Display whether the number is odd or not.
Ask the user if they want to check another number.
Repeat the process if the user enters Y, and exit with a thank-you message if the user enters N.
Handle invalid inputs for the continuation prompt (Y/N) gracefully.
```bat
@echo off

:START
cls
set /p num=Enter a number: 

set /a rem=%num% %% 2

if %rem%==0 (
    echo The number is NOT odd.
) else (
    echo The number is odd.
)

:CHOICE
echo.
set /p choice=Do you want to check another number? (Y/N): 

if /I "%choice%"=="Y" goto START
if /I "%choice%"=="N" goto END

echo Invalid input! Please enter Y or N.
goto CHOICE

:END
echo Thank you for using the program!
pause
```

<img width="606" height="232" alt="image" src="https://github.com/user-attachments/assets/b1ac23c4-0e23-47ad-af20-dcff67d5c05c" />


## OUTPUT




Write a batch file that uses a FOR loop to iterate over a sequence of numbers (1 to 5) and displays each number with the label Number:. The output should pause at the end.

```
bat id="q7m2xs"
@echo off

for /L %%i in (1,1,5) do (
    echo Number: %%i
)

pause
```



## OUTPUT
<img width="826" height="287" alt="image" src="https://github.com/user-attachments/assets/c5bf6ef8-848f-46d9-8474-07ff4d8a8128" />




Write a batch script to check whether a file named sample.txt exists in the current directory. If the file exists, display the message sample.txt exists. Otherwise, display sample.txt does not exist. Pause the script at the end to view the result.

Instructions:
Use the IF EXIST conditional statement.
Make sure the script works for files located in the same directory as the batch file.
Use pause to keep the command window open after displaying the message.
Expected Output (if the file exists):
```bat id="c8m2zr"
@echo off

if exist sample.txt (
    echo sample.txt exists
) else (
    echo sample.txt does not exist
)

pause
```

## OUTPUT
<img width="507" height="114" alt="image" src="https://github.com/user-attachments/assets/9e95f7dd-aad6-4944-a6b2-37bb7e39f09e" />

<img width="545" height="96" alt="image" src="https://github.com/user-attachments/assets/4171105b-7b1f-4340-a0ad-786ac41f3103" />

Write a batch script that displays a simple menu with three options:
Say Hello – Displays the message Hello, World!
Create a File – Creates a file named newfile.txt with the content This is a new file
Exit – Exits the script with a goodbye message
The script should repeatedly display the menu until the user chooses to exit. Use goto statements to handle menu navigation.

```
@echo off

:MENU
cls
echo ===== MENU =====
echo 1. Say Hello
echo 2. Create a File
echo 3. Exit
echo =================
set /p choice=Enter your choice (1-3): 

if "%choice%"=="1" goto HELLO
if "%choice%"=="2" goto CREATE
if "%choice%"=="3" goto EXIT

echo Invalid choice! Please try again.
pause
goto MENU

:HELLO
echo Hello, World!
pause
goto MENU

:CREATE
echo This is a new file > newfile.txt
echo File newfile.txt created successfully.
pause
goto MENU

:EXIT
echo Goodbye!
pause
exit
```

## OUTPUT
<img width="537" height="281" alt="image" src="https://github.com/user-attachments/assets/fa91e491-d7ad-4ede-b5a8-047a0b5b007b" />



# RESULT:
The commands/batch files are executed successfully.

