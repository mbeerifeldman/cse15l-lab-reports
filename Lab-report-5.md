# Lab Report 5
### Maya Beeri-Feldman

## Part 1 
1. 
Hi, keep getting this weird output for a symptom for some bug. I've written tests for my ListExamples method, but the result is not what I expected so I think there might be some bug in my ListExamples.java code.
It think the bug is that I am not correctly updating my index in my looping merge function since the values are not being ordereded correctly. Could you please help me with whether I'm the write path or not?
Thanks in advance. 
![image](https://github.com/mbeerifeldman/cse15l-lab-reports/assets/114952150/d6c3ddf2-adb7-4e58-a570-222688578bed)

2. 
Hi, I think it might be helpful for you to take a deeper look at the values your TestListExamples is storing to see if helps with looking at
what the problem is. It might be helpful to use the jdb debugger to see what values are being stored in your parameters. Is there something obvious that
stands out when looking at the two unmerged lists and the merged lists side by side? The debugger can be helpful with looking at this. Good luck!

4. 
Ok! I added in jdb command to my bash script to see what values are being stored in my first test of the merge method. Based on these results,
I can clearly see that the merged and expected are created with separate IDs and that what's printing is the left followed by the right. So
I think the bug is that there isn't a proper comparison such that the issue must either be with entering the while loop or something else in
its body like the if statement. This pointed me to find the actual bug in my while statement comparing the two loops, finding that
the logic for it was wrong. I had the greater than equal sign being used instead of the less than sign and this caused the while loop to never enter as
the first index wasn't greater than the size of the input list and instead dropped down to just file in the merged list by going through the provided lists. Thank you for the help.
<img width="460" alt="Screen Shot 2023-12-02 at 4 31 30 PM" src="https://github.com/mbeerifeldman/cse15l-lab-reports/assets/114952150/d6f851ac-e027-4668-98ba-b1d582fc34fb">

6. 
The files needed were in the `grade-review-mbeerifeldman` repo which held the `grade.sh` file that was used to use the tests in the `TestListExamples.java` file.
The directory to access these files was originally the home one but after using `git clone` on the repo, I was then able to use `cd` to get into the `*/grade-review-mbeerifeldman` directory from the home directory to run `bash grade.sh`. Other files other then `grade.sh` and `TestListExamples.java` which were needed was `ListExamples.java` which was accessed through a repo only containing that file and passed as an argument to `grade.sh`. Additionally the grade-review repo also contains a grading area to transport all the .java files into and a folder containing the junit packages. Such that as an end result we end with directory structure created by `grade.sh` storing the files `student-submission/* ` `lib/ ` and `TestListExamples.java` all in `grading-area/`, where `grading-area`
is a directory that is (first cleared and then) made upon each run of `grade.sh` used to store the passed in `ListExamples.java` file (stored in `student-submission` folder) and all the rest of
the files present in `lib` (junit) and `TestListExamples.java`. 


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

The contents of `TestListExamples.java` before debug

```
import static org.junit.Assert.*;
import org.junit.*;
import java.util.Arrays;
import java.util.List;

class IsMoon implements StringChecker {
  public boolean checkString(String s) {
    return s.equalsIgnoreCase("moon");
  }
}

public class TestListExamples {
  @Test(timeout = 500)
  public void testMergeRightEnd() {
    List<String> left = Arrays.asList("a", "b", "c");
    List<String> right = Arrays.asList("a", "d");
    List<String> merged = ListExamples.merge(left, right);
    List<String> expected = Arrays.asList("a", "a", "b", "c", "d");
    assertEquals(expected, merged);
  }
  @Test(timeout = 500)
        public void testMerge() {
        List<String> input1 = Arrays.asList("b", "c", "d");
        List<String> input2 = Arrays.asList("a", "d", "e", "e", "e");
        List<String> input3 = Arrays.asList("a", "b", "c", "d", "e", "e", "e");

        assertEquals(input3, ListExamples.merge(input1, input2));
        }
}
```

And contents of `ListExamples.java` before debug: 

```
import java.util.ArrayList;
import java.util.List;

interface StringChecker { boolean checkString(String s); }

class ListExamples {

  // Returns a new list that has all the elements of the input list for which
  // the StringChecker returns true, and not the elements that return false, in
  // the same order they appeared in the input list;
  static List<String> filter(List<String> list, StringChecker sc) {
    List<String> result = new ArrayList<>();
    for(String s: list) {
      if(sc.checkString(s)) {
        result.remove(0);
      }
    }
    return result;
  }


  // Takes two sorted list of strings (so "a" appears before "b" and so on),
  // and return a new list that has all the strings in both list in sorted order.
  static List<String> merge(List<String> list1, List<String> list2) {
    List<String> result = new ArrayList<>();
    int index1 = 0, index2 = 0;
    while(index1 > (list1.size()) && index2 < list2.size()) {
      if(list1.get(index1).compareTo(list2.get(index2)) < 0) {
        result.add(list1.get(index1));
        index1 += 1;
      }
      else {
        result.add(list2.get(index2));
        index2 += 1;
      }
    }
    while(index1 < list1.size()) {
      result.add(list1.get(index1));
      index1 += 1;
    }
    while(index2 < list2.size()) {
      result.add(list2.get(index2));
      // change index1 below to index2 to fix test
      index2 += 1;
    }
    return result;
  }


}
```

Command line to trigger bug:

```
bash grade.sh https://github.com/mbeerifeldman/listmethods.git
```


How to debug:
First add run jdb on TestListExamples.java to see the values that are being stored. Then after deducing what the symptom is in more detail, know where to look for bug 
(which while loop specifically) and then change the logic in the while loop, successfully correcting it so that it will run. 

Adding jdb to bash file:
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

Fixing while loop:
```
while(index1 < (list1.size()) && index2 < list2.size()) //now both are less than and loop should run
```

## Part 2

I did not know about the amazing abilities of vim. I find it to be very useful when working without the phyiscal files being present, and thus being able to just use the command 
line to edit files. I had no knowledge of vim before this class, but with just a few commands memorized, I think it's very helpful. I also had no knowledge of jdb before this class
and find that using it is very helpful for getting to take a deeper look at the code but also helpful with just laying out
what values each variable has in a clear way. 




