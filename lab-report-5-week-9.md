```

# Create your grading script here

rm -rf student-submission
git clone $1 student-submission
RESULT="0"

# check if contains the file ListExamples.java
cd student-submission
if [ -f ListExamples.java ]
then
    echo "ListExamples.java file found"
else
    echo "ListExamples.java file not found"
    echo "Result is: "$RESULT
    exit 1
fi

cd ..
cp -r lib student-submission/
cp TestListExamples.java student-submission/
cd student-submission
javac -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar *.java

# checks if the code complies
if [ $? -eq 00 ]
then
    echo "Compilation succeeded"
else
    echo "Compilation failed"
    echo "Result is: "$RESULT
    exit 1
fi

java -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar org.junit.runner.JUnitCore TestListExamples

#checks if its passes all the test cases written in ListExamples.java
if [ $? -eq 00 ]
then
    RESULT=2
    echo "Result is: "$RESULT
else
    echo "Result is: "$RESULT
fi

```
**Screenshots of the files testing my grade script** 

1.https://github.com/ucsd-cse15l-f22/list-methods-corrected, which has the methods corrected (I would expect this to get full or near-to-full credit)

<img width="772" alt="Screen Shot 2022-11-28 at 1 42 47 AM" src="https://user-images.githubusercontent.com/100493743/204247910-a377b4c8-f867-4701-a5ea-6726da506b29.png">


2.https://github.com/ucsd-cse15l-f22/list-methods-compile-error, which has a syntax error of a missing semicolon. 

<img width="784" alt="Screen Shot 2022-11-28 at 1 42 21 AM" src="https://user-images.githubusercontent.com/100493743/204248091-7383f33e-2e0f-4c83-a0bd-dc4862c80589.png">

3.https://github.com/ucsd-cse15l-f22/list-methods-filename, which has a great implementation saved in a file with the wrong name.

<img width="812" alt="Screen Shot 2022-11-28 at 1 41 49 AM" src="https://user-images.githubusercontent.com/100493743/204248290-2175ff34-03aa-4446-aef2-bbe259a92187.png">

Tracing the path for the repository with the wrong file name:

 |**Comamand**     |**Standard output**     |**Standard Error**                         |**Exit Code**  
 _____________________________________________________________________________________________________
 
 |rm -rf           |   -                    |   -                                       |0
__________________________________________________________________________________________________                                                                
 |git clone        |   -                    |   Cloning into 'student-submission'...    |0
 _____________________________________________________________________________________________________

 |cd               |   -                    |   -                                       |1

2. The first if statement that checks if the directory contains the file is false because this repository does not contain the ListExamples.java
 
   The second if statement which check if the code complies is true but does not run due to the early exit for the code
   
   The third if statement which checks if it passes the test case is true but it doesn not run due to an early exit from the script
   
3.These code lines do not run-

```
cd ..
cp -r lib student-submission/
cp TestListExamples.java student-submission/
cd student-submission
javac -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar *.java

# checks if the code complies
if [ $? -eq 00 ]
then
    echo "Compilation succeeded"
else
    echo "Compilation failed"
    echo "Result is: "$RESULT
    exit 1
fi

java -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar org.junit.runner.JUnitCore TestListExamples

#checks if its passes all the test cases written in ListExamples.java
if [ $? -eq 00 ]
then
    RESULT=2
    echo "Result is: "$RESULT
else
    echo "Result is: "$RESULT
fi
```
