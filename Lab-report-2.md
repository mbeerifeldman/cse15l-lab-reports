# Lab Report 2
### Maya Beeri-Feldman

## Part 1

![image](https://github.com/mbeerifeldman/cse15l-lab-reports/assets/114952150/1a365746-5ac9-49b4-9537-bfffd4ea8502)
![image](https://github.com/mbeerifeldman/cse15l-lab-reports/assets/114952150/247c1f86-842e-475d-8371-91674b9f2f9d)

![image](https://github.com/mbeerifeldman/cse15l-lab-reports/assets/114952150/db81d6ff-15ac-4dca-86b6-f7629b3a8708)

> The methods called are `handleRequest` and `main`. The relevant arguments to `handleRequest` is the URI or current `URL`/`url` whereas
> the relevant values are the `url` belonging to `URI`, the `String s`, the `int num` and the `String s1` and the `String array parameters`.
> `url` reflectes the current url inputted while `String s` holds all of the strings inputted so far as one string.
> `num` counts up with each string, or successful url passed and `s1` gets rid of the `+` stored with the `url`.
> `Parameters` keeps track of what was input into the url.

> The values will change based on user input and based on how many inputs. One reason no values would get changed was if
> the `url` did not get the necessary argument needed of `/add-message?=` followed by a string. Otherwise, the algorithm is set up
> such that each time a URL is passed, it will update first its new `url` then take the string part of it and remove all
> the pluses and then add this onto the current string holding all of the previous responses. It gets added then using the int value
> which counts how many strings have been added.

## Part 2 

![image](https://github.com/mbeerifeldman/cse15l-lab-reports/assets/114952150/89acdec9-f9cd-44c2-b9b7-59a17c2f72f6)
Logging in without password
![image](https://github.com/mbeerifeldman/cse15l-lab-reports/assets/114952150/cbae18a8-1d89-400b-a9da-e214031eade6)
private key or /User/Bluestarr/.ssh/id_rsa
![image](https://github.com/mbeerifeldman/cse15l-lab-reports/assets/114952150/6f89f50e-c876-41e3-bd99-543ece8fc501)

public key or /User/Bluestarr/.ssh/id_rsa.pub


## Part 3
One thing I learned was the usage of man which when paired with a command will show a manual of that commands. I think such a featured
can be very helpful in learning about how to use a command from the terminal. I also learned about how "\n" creates a new line in code and
how Java knows to read this command not as a string but as a line break. 
