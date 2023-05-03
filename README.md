Download Link: https://assignmentchef.com/product/solved-cs332-lab5-process-synchronization
<br>
<strong>Lab 5 – Process Synchronization</strong>

The given bank.c program has 3 processes namely, the <em>dad </em>process and two <em>son </em>processes. The critical section (CS) in the given problem is a son withdrawing money from the bank and the dad depositing money in the bank, at randomly selected time intervals. The program in the given form has synchronization errors, i.e., these 3 processes get into a race condition when accessing the shared bank_balance variable. The program itself compiles correctly (i.e., there are no syntax errors).

In <strong>Step 1</strong>, you need to run the program and analyze the execution traces, whereupon you have to identify the synchronization errors. After identifying the synchronization errors, you need to insert the “P(sem)” and “V(sem)” operations at the right places in the code that fix the synchronization errors.

In <strong>Step 2</strong>, you work on a measurement component. A mutex algorithm is associated with a “bounded wait” property, i.e., how long a process P is forced to wait for entry into a CS after P has expressed interest in the CS. Let’s call the wait time T(P), where T(P) is the number of times processes other than P enter the CS after P expresses interest in the CS but before P actually enters the CS. You need to compute T(P) for all three processes in the problem and display it at the end of “N” different attempts. Measure T(P) for at least 5 different N’s and include the values in your report.

<h1>Instructions</h1>

<ul>

 <li>There are two different interfaces to semaphores in the POSIX standard: POSIX 1003.1b semaphores and System V semaphores. In this lab, we will use System V semaphores. The lab drive folder has the file “sem.h” that contains the usual create, destroy, P (or wait), and V (or signal) operations for System V semaphores which would be used to fix synchronization errors.</li>

 <li>You need to have sem.h header file in your present working directory to run this program and invoke semaphore operations.</li>

 <li>The bank.c file is documented. Once you are done with your solution, insert comments at the places where you made changes to fix the synchronization errors and add the wait time measurement.</li>

 <li>This synchronization problem should be solved with as few semaphore variables as possible.</li>

</ul>