# Timetable-Organiser


Task:

Timetable Organiser is a system that allows users to view university timetables in multiple forms including by campus, room, subject, and lecturer. The system expects the timetable data to be stored in a simple comma-separated text file with the format: 

subject,activity,day,start,end,campus,room,lecturer

A sample timetable data file is shown below:

```
ABC101,Lecture,Monday,08:00,10:00,Jenolan,J10112,Ada Log
ABC101,Tutorial,Tuesday,10:00,11:00,Jenolan,J10115,Ena Blue
ACE204,Lecture,Monday,09:00,11:00,Tarana,T05201,Kin Wall
ACE206,Lecture,Wednesday,13:00,14:00,Tarana,T06402,Kin Wall				
PRG321,Lecture,Tuesday,14:00,16:00,Jenolan,J09302,Foxy Rex				
PRG321,Tutorial,Thursday,11:00,12:00,Jenolan,J09212,Esk Brown
```

You are required to develop a menu-based program that implements the Timetable Organiser system. Your program should prompt the user for a timetable data file name. After the file has been successfully read, the system will interact with the user to view the timetable according to the desired selections.

Review the sample run below to clearly understand the requirements.

```
Timetable Organiser
-------------------

Enter the timetable data file name: timetable-sample.txt
** Reading timetable data ...
** Success!

Timetable menu
--------------
[C]ampus
[R]oom
[S]ubject
[L]ecturer

> Enter selection or [Q]uit: L

Lecturers
---------
[1] Ada Log
[2] Ena Blue
[3] Kin Wall
[4] Foxy Rex
[5] Esk Brown

> Enter selection: 3

Timetable for lecturer "Kin Wall": 
===============================================================
Subject Activity Day       Start End   Campus   Room   Lecturer
---------------------------------------------------------------
ACE204  Lecture  Monday    09:00 11:00 Tarana   T05201 Kin Wall
ACE206  Lecture  Wednesday 13:00 14:00 Tarana   T06402 Kin Wall				
===============================================================


Timetable menu
--------------
[C]ampus
[R]oom
[S]ubject
[L]ecturer

> Enter selection or [Q]uit: c

Campuses
--------
[1] Jenolan
[2] Tarana

> Enter selection: 1

Timetable for campus "Jenolan":
===============================================================
Subject Activity Day       Start End   Campus   Room   Lecturer
---------------------------------------------------------------
ABC101  Lecture  Monday    08:00 10:00 Jenolan  J10112 Ada Log
ABC101  Tutorial Tuesday   10:00 11:00 Jenolan  J10115 Ena Blue
PRG321  Lecture  Tuesday   14:00 16:00 Jenolan  J09302 Foxy Rex	
PRG321  Tutorial Thursday  11:00 12:00 Jenolan  J09212 Esk Brown
===============================================================


Timetable menu
--------------
[C]ampus
[R]oom
[S]ubject
[L]ecturer

Enter selection or [Q]uit: q

Have a nice day!
```

Your program must validate the timetable data file before proceeding. Specifically, your program must verify the following:

each line consists of exactly eight fields separated by commas
subject and room fields must be alphanumeric strings starting with a letter
activity, day, campus and lecturer fields must be alphabetic strings
If any of these conditions is not satisfied, the program should display an error message and quit.

Below is a sample run when an incorrectly formatted file is provided.

```
Timetable Organiser
-------------------

Enter the timetable data file name: timetable-sample-incorrect.txt
** Reading timetable data ...
** Error! File is not correctly formatted.


Have a nice day!
```
Constraints

 * You must define a function called display_timetable that accepts a string parameter containing the selection type and a list parameter containing the selection results, and prints the table in the format shown in the sample above.
 * You must use lists and string methods in your program.
 * You must handle the IOError exception with a specific handler. In addition, your program must not crash regardless of the input provided.
 * Your program must not import any library or module other than your own written modules (if any).

**Task 1 (15 marks)**

Implement your program in Python. Comment on your code as necessary to explain it clearly. 

**Task 2 (5 marks)**

Select at least three sets of test data that will demonstrate the normal operation of your program; that is, test data that will demonstrate what happens when a valid input is entered. Select two sets of test data that will demonstrate the abnormal operation of your program; that is, test data that will demonstrate what happens when an invalid input is entered or when an error is encountered.

Set it out in a tabular form as follows: test data type, test data, the reason it was selected, the output expected due to using the test data, and finally a screenshot of the output actually observed when the test data is used. It is important that the output listings (i.e., screenshots) are not edited in any way.
