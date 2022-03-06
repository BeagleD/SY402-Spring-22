# SY402-Spring-22
Lab 5 - Understanding the Host's Integrity

We have discussed Host Integrity as a tool in our network defense in depth. By checking Host files for changes - expected and unexpected - you can see what changes are going on and spot adversarial behavior. 

The objective of this lab is to write software in your Github account  that will detect changes across the filesystem in your Kali VM you are using for SY402 by hashing all of the filles. This is accomplished by writing a Python script that will walk through all of the directories on your Kali VM and hash each individual file, keeping track of the hash values so that subsequent runs can make note of the changes. In essence, you are writing a software package similar to the initial tripwire software.

You can then create some changes (for example by running updates or upgrades) - re-run the program and see what changes occur. 


Problems
1. Create a hash.py script in your Github account you previously created  that will recursively walk through all files on your VM. You should be able to configure your program to define certain files and/or directories as unhashable so they will be ignored. 
Kali Linux File Structure:



/dev is a perfect example, as you do not want to hash this directory. Note: Below is a non-exhaustive list of directories you will probably want to ignore (if your program gets stuck on a directory you will want to consider ignore those as well):


 /dev
/proc
 /run 
/sys 
tmp 
/var/lib 
/var/run 

A Part 1 solution will be able to walk through the entire file system, printing out the filenames with their paths and taking no action (but skipping) the unhashable directories. You do not need to start from scratch - recall our discussion of modern software development - you can find libraries and functions such as  os.listdir, os.stat, and os.walk can be quite helpful. BE SURE TO COMMENT AND DOCUMENT YOUR SOURCES! 


2. Integrate SHA2 (SHA256) so that each file is hashed as it moves through the file system. You are not
expected to write SHA2 from scratch, use a python library such as hashlib.

3. Store the file and hash information so that it will be available for future runs. At a minimum store the
following data:

filename with full path
hash
date/time file was observed


4. The final step, your program should run and update the hash information, upon completion it should print out summary information that includes all new files found, any missing files, and any file that was modified
.
5. Extra Credit: Detect that a file was moved, add to your summary section an output that documents where the file is now, and where it was, and the time of the last scan that saw it in the older location.

What to Submit:

Post your program in your github account - and then run as per the steps above including screen shots demonstrating each successful step from your VM along the way on this lab - saved as a pdf and uploaded to Blackboard. Be sure to include your name and section on the report - and answer the feedback questions below. 

Lab FEEDBACK Questions
1. How long did this assignment take you to complete, outside of class? 



2. Collaboration – list anyone you talked to about this assignment (aside from instructor), or any online/written sources consulted (aside from the textbook or lecture notes). Enter “none” if appropriate. 


3. What was the most important thing you learned about in this assignment? 




4. What was the best part about this assignment? 




5. The worst? 


6. Do you think your assignment is… (bold/color one)

Fully Completed 

Partially Completed 

If you marked “Partially completed”, why is it not completed? 
Example: Didn’t start soon enough- Too busy with other things - Was harder than I expected - Didn’t understand directions - Didn’t understand the concepts 
Other (discuss):



Was this assignment: (circle one):
Way too easy               Little too easy           About right                Little too hard   Way too hard 

 Any other comments or suggestions? 


