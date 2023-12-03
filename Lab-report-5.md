# Lab Report 5
### Maya Beeri-Feldman

## Part 1 
1. 
Hi, keep getting this weird output for a symptom for some bug. I've written tests for my ListExamples method, but the result is not what I expected so I think there might be some bug in my ListExamples.java code.
It think the bug is that I am not correctly updating my index in my looping merge function since the values are not being ordereded correctly. Could you please help me with whether I'm the write path or not?
Thanks in advance. 
![image](https://github.com/mbeerifeldman/cse15l-lab-reports/assets/114952150/d6c3ddf2-adb7-4e58-a570-222688578bed)

2. 
Hi, I think it might be helpful for you to trace through the function and with your test to simulate what you think the code should be doing at each step. It might be helpful to use
the jdb debugger to see what values are being stored in your parameters. Good luck!

3. 
Ok! I added in jdb command to my bash script to see what values are being stored in my first test of the merge method. Based on these results,
I can clearly see that the merged and expected are created with separate IDs and that what's printing is the left followed by the right. So
I think the bug is that there isn't a proper comparison. This let me find the bug in my while statement comparing the two loops, finding that
the logic for it was wrong. I had the greater than equal sign being used instead of the less than sign and this caused the while loop to never enter as
the first index wasn't greater than the size of the input list and instead dropped down to just file in the merged list by going through the provided lists.
<img width="460" alt="Screen Shot 2023-12-02 at 4 31 30 PM" src="https://github.com/mbeerifeldman/cse15l-lab-reports/assets/114952150/d6f851ac-e027-4668-98ba-b1d582fc34fb">

4. j
The files needed were in the `grade-review-mbeerifeldman` repo which held the `grade.sh` file that was used to use the tests in the `TestListExamples.java` file.
The directory to access these files was used by cloning the repo and then using `cd` to get into the `*/grade-review-mbeerifeldman` directory from the home
directory.
The contents of grade.sh before fix:

```
CPATH=".:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar"

rm -rf student-submission
rm -rf grading-area

mkdir grading-area

git clone $1 student-submission
echo 'Finished cloning'

# Draw a picture/take notes on the directory structure that's set up after
# getting to this point

# Then, add here code to compile and run, and do any post-processing of the
# tests

if [[ -f student-submission/ListExamples.java ]]
then
  echo 'Correct file provided'
else
  echo "Haven't provided the correct file"
  exit 0
fi

cp -r student-submission/* grading-area/
cp -r lib/ grading-area/
cp -r TestListExamples.java grading-area/

cd grading-area

javac -cp "$CPATH" *.java
java -cp "$CPATH" org.junit.runner.JUnitCore TestListExamples >> results.txt

if [[ `grep "FAILURES!!!" results.txt` ]]
then
    echo "Tests did not all pass."
    echo `tail -n 3 results.txt`
else
    echo "All tests passed! Nice job."
fi
```


How to debug:

```

then
    echo "Tests did not all pass." 
    cat results.txt
    javac -g -cp "$CPATH" *.java
    jdb -classpath "$CPATH" org.junit.runner.JUnitCore TestListExamples
else
    echo "All tests passed! Nice job."
fi
```
And then based on this 


