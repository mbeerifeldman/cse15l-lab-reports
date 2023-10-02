# **Lab Report 1**
### Maya Beeri-Feldman 

## cd

1. ![image](https://github.com/mbeerifeldman/cse15l-lab-reports/assets/114952150/b5755966-2c9c-48a3-93a2-16593f827115)
> The current directory was simply the default working space. Since there are no arguments given, the directory does not change to anything. This is not an error, but the expected behavior since I have not given any arguments for the current directory, so it should stay the same.
   
2. ![image](https://github.com/mbeerifeldman/cse15l-lab-reports/assets/114952150/74ba503e-3ece-4a40-8810-ac206e01f121)
> The working directory was the default. Since the argument was the folder lecture1, the directory changes to that so the output is the new directory using the argument that I gave it. This is not an error as I navigated to the directory that I wanted using the argument. 
   
3. ![image](https://github.com/mbeerifeldman/cse15l-lab-reports/assets/114952150/e1c5ee3e-1085-4b63-b064-d197f4a325fc)
> The working directory was the two files that I git cloned such that I could access the file. The output was that my file is not a directory such that the cd did not work and didn't navigate to something different. Thus this resulted in an error message, it is not technically unexpected as this is what happens when you try to cd something that isn't a directory/folder but rather a file. 

## ls

1. ![image](https://github.com/mbeerifeldman/cse15l-lab-reports/assets/114952150/4677e0a5-1658-4f00-b194-4c081218d55e)
> The working directory was the folder messages. The output with no argument gave the listed contents of the cd which in other words was the four txt files I had in that folder. This is the expected outcome and not an error as these are the files in that folder that were outputed which is what the ls command does.

2. ![image](https://github.com/mbeerifeldman/cse15l-lab-reports/assets/114952150/021516ab-89ab-48ca-ab4b-550f718fb574)
> The working directory was the folder lecture1. The output with argument messages gave me the contents of that folder, specifically the four txt files. This is the correct output as it gave me the listed items in that folder (just like my first image which also used messages; both of these correctly gave me the listed items in messages.)

3. ![image](https://github.com/mbeerifeldman/cse15l-lab-reports/assets/114952150/8f5279dc-9bf5-4f24-a77f-dc63a7206a7a)
> The working directory was messages folder. The output listed out the file itself which was the argument. This makes sense as there is not an files stored in that file as it is not a folder. It simply lists what is given as there is nothing else inside it which is what I would expect and thus not an error. 

## cat

1. ![image](https://github.com/mbeerifeldman/cse15l-lab-reports/assets/114952150/29074966-8f43-433b-a190-e0d91f806c14)
> The working directory is the default one. The output is a break in the command. This happens because the cat command relies on being give at least one file such that it can return its output. This is an error caused by the command not being used properly.

 2. ![image](https://github.com/mbeerifeldman/cse15l-lab-reports/assets/114952150/d3c295e0-a6db-418a-8c9c-1187983465d5)
> The working directory is the default one. The output is an error messages. This occured because the command cat expects to be given a file that it can read from. In this case I provided it with a directory and not a file so the error is that it was not given the correct argument.

3. ![image](https://github.com/mbeerifeldman/cse15l-lab-reports/assets/114952150/4ab80d5f-a2a7-40e1-a86c-7958049c3638)
> The working directory is the messages folder. The output is the current content that is in the given file (en-us.txt). This output is not an error because cat expects at least one file and that was the argument it was given so it was able to print out this result. 



   



