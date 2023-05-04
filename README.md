Download Link: https://assignmentchef.com/product/solved-cs585-hw2-code-solutions-to-the-ve-sql
<br>
Total points: 5*1=5, plus 2 add’l points, but with a CAP of 5 points [if you score 6, or 7, your score would ‘only’ be a 5].

In this assignment, you will code solutions to the <strong>ve</strong> SQL problems described below. Guess what – the questions relate back to HW1 here, you’re asked to create tables and data to get the STEM tutoring business going, and perform queries on the data (like the business owner would).

ALL the SQL knowledge/commands you need to answer the questions have been covered in class! You <strong>do NOT</strong> need to learn more commands or techniques (eg. use of ‘triggers’) etc. on your own in order to do this HW set.

To run SQL code, you can use one of the three ways mentioned in the lecture notes [a locally installed DB, or a remote server-based DB via an online shell running in a browser page, or a cloud DB] to do the problems.

One more cloud-y way, not mentioned in class, to do your homework (and continue learning and practicing SQL) is to use <a href="https://livesql.oracle.com/">https://livesql.oracle.com/ (https://livesql.oracle.com/);</a> after you sign up for a free account, you can create tables, insert rows and do queries – you can save all your work in separate sessions, reload [any/all of] them after logging in again in order to recreate your tables+data and rerun queries, and also add more tables/data/code to the mix – it’s very convenient and cool, try it!

<strong>What you need to submit are text les with the SQL commands that you come up with, one le for each question (Q1.sql, Q2.sql.. Q5.sql).</strong> PLEASE MENTION AT THE TOP OF EACH FILE, which database (eg. Oracle, SQLite..) you used for that question! Your grader(s) will execute the SQL commands from the text les you

submit, using the same <sub>Loading [MathJax]/extensions/MathZoom.js</sub>software you used, to see if they produce the expected results.

You can talk to your friends/classmates to informally discuss approaches to the problems, but DO NOT {‘share’/look up/ask others for} actual code – that would be plagiarism, and will get you an ‘F’ in the course.

Please see your TAs/graders if you need one-on-one help (or see me). You can also post (and reply!) in the Piazza ‘hw2’ forum. Don’t wait, start early. Good luck, have fun!

<strong>Q1 .</strong> To work on their projects, each student group (who sit in numbered tables, as described in HW1) can also (in addition to working at those numbered tables) reserve one of ten available rooms to work on their project. The rooms can be reserved for a block of a few hours (eg. 3 hours), with a start time and end time, eg. 3pm-6pm, 9am-2pm etc. At the end of the day, everyone goes home, so there’s no possibility of rooms being booked for multiple days. The table structure you are asked to use, is this:

There are two problems (issues) with the above. First, the start time could be incorrectly entered to be later than the end time. Second, a new entry (for a new group) could be accidentally put in to occupy a room, even before the existing group in that room is done using that room. For simplicity, you can express times in the 24h militarystyle format, eg. 9 for 9AM, 17 for 5PM, etc. For further simplicity, all bookings start and end ‘on the hour’, so, ints between 7 (7AM) and 18 (6PM) should be su     cient.

How would you <strong>redesign the table</strong> to x both these issues? For your answer, you can either provide a textual explanation, and/or provide SQL statements. Hint – “do not be concerned with e ciency” – ANY working solution is acceptable &#x1f642;

Loading [MathJax]/extensions/MathZoom.js

<strong>Q2 </strong> Given the following portion of the enrollment table, <strong>write a query</strong> to create a listing that includes class name and the number of students enrolled in the class, sorted in reverse order of enrollment (eg. to tell which were the most popular classes, at the end of the term).

Given something like the above, the output could be:

<strong>Q3 .</strong> Below is a small table that tracks work being done on the students’ projects. We have a project ID column on the left, a ‘step’ column in the middle (0,1,2.. denote steps of the project), and a status column on the right (where ‘W’ denotes ‘waiting’, ‘C’ denotes ‘completed’). Such a table lets project instructors get a quick status on the various aspects (steps) of their projects (“where




they’re at”, in colloquial, ungrammatical language). Speci cally, ‘W’ would mean that the students are stalled for whatever reason (don’t understand what to do, a part broke, they have bugs they can’t x, etc) and need additional help from the instructors – students would have a way to input these (step number, status), and instructors can review the table periodically and run queries like the one you will be creating.

<strong>Write a query</strong> to output the project(s) where only step 0 has been completed, ie. the project gotten started but the rest of the steps are in waiting mode. In the above table, such a query would output just ‘P100’. You can assume that steps get completed in order, ie. P333 will never have C,W,C,W for example [all Cs will occur before all Ws].

<strong>Q4.</strong> Below is a small sample of a junkmail database we own, ie. people we want to ‘spam’ via postal mail to get them to enroll their kids in our STEM academy [lol].

Each entry consists of a name, address, ID, and whether there is a prior family member already in the db; in the last column, NULL means that entry is the rst family member in our db, and a non-null value is the ID of the rst family member (eg. Diego points to Alice, and Ella points to Bob).

<strong>Write a query</strong> to delete from the table, names that have ‘NULL’ for SameFam <strong>and</strong> another family member in the db. So in our example above, the query would delete Alice and Bob, but not Carmen and Farkhad. In other words, we want to save postage by only sending one mail per household if we have two people from a house in our db (we assume that our db contains either one person per household, or two).

<strong>Q5 .</strong> We post job descriptions, to build a list of quali ed instructors we can pick from. Here’s an abbreviated table of possible candidates, with just their name and the subject(s) they can teach:

<strong>Write a query</strong> that will pick out just the instructors who can teach every subject in the table below (this is so we can hire a small number of instructors who would be easy to manage, compared to a larger group) – we’re deciding to o   er just the classes listed below:

With the above data, the query would output

You can hardcode the subjects just for submission purposes, but your query should work for ANY such table! Using comments in the code, <strong>YOU NEED TO EXPLAIN IN YOUR OWN WORDS, WHAT THE</strong>

<strong>QUERY DOES</strong> (how it works); don’t just say things like “Now I’m using a WHERE condition”, instead explain what it’s for (why you’re using it).

<table>

 <tbody>

  <tr>

   <td width="53"></td>

  </tr>

  <tr>

   <td></td>

   <td></td>

  </tr>

 </tbody>

</table>

<strong>Bonus(1(+1) point(s))</strong>. You will get 1 extra point if you can reformulate the query in a <strong>very di      erent way</strong>! If you do this, submit a separate text le with the code, eg. Q5_v2.sql. If you come up with <strong>YET ANOTHER very di erent way</strong>, you can get 1 more bonus point (submit yet another le, eg. Q5_v3.sql). ‘Very di     erent’ means just that – the approaches do have to be totally distinct, eg. you can’t use NOT to invert an existing solution, or use IN() instead of OR, etc. Sooo… is this actually possible [to do it in two, or three, di      erent ways]? <strong>Yes!</strong> Or, as they say in Minne-so-ttta – “yooo betcha!”

To reiterate, everything you need is in the slides (the material we went through in class) – you do not need to read ahead or look up more commands online! Look at each relational operator, each command, each function, each keyword that we covered, and ask yourself how it could be of use in constructing your query.