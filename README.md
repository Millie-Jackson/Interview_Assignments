# Interview_Assignments
Various task solutions from interviews. Inludes thought processes and discussion

XAPIEN

TASK

Background: Every time one of our users runs a report our Search & NLP pipeline fetches loads of information about them from company records, news articles, and blog posts. After completing this it will be able to generate a list of all company names it’s seen, we want to deduplicate entries in this list, so that our Report Generation pipeline can group together information about the same company before displaying it to the user.

Task: Write a function which takes in a list of company/organisation names, and reduces the list to one entry per company. Lots of companies will be in their multiple times, possibly with different forms of their names. The file provided should be treated as a representative example of the list of names your function will receive. You should carefully consider the time complexity of your code.

Include unit tests to show that your function works on various edge cases. The problem is fairly ill-defined and open ended, so part of the challenge is to define some bounds for your work! We're not looking for a complete solution - just a decent stab, a few good ideas and some sensible code.

Feel free to import and use any libraries or external datasets you like - that's a key part of real-world software development.

You should take care to ensure your code is readable and well-commented where necessary. Share your code (the whole solution, including the tests) with us (zip in an email, or public GitHub project). Please also share with us any additional comments, thoughts, or ideas about any difficulties you encountered in this task, and please take care to explain any limitations of your solution which you're aware of.

STEPS
- Write a function
- Function takes in a list
- Reduce the list to 1 entry per company
- Consider time complexity
- Unit tests prooving it deals with edge cases
- Readable and well commented
- Share ideas and difficulties
- Explain limitations

IDEAS
Use a set or dictionary to remove duplicates automatically
Store the size of the list to compare after cleaning to see how many duplicates were removed
Use a decorator to time the function
Use wildcards to remove unnecessary words
Remove obvious words (without editing them) like 'LIMITED' and 'LTD'
Do as few cycles of the list as possible to maintain speed
Refactor funtion into smaller functions?
Rewrite function timer to take an average of 3

QUESTIONS
Is transfering to a set less speedy than transfering to a dictionary?
Is there a method for removing duplicates? (Pandas? NumPy?)
Test a random section instead of the whole document to reduce time?
Would a generator be useful?
Would RegEx be useful?
Some of the items are in caps, does case matter?

ANSWERS
A set is slower than a dictionary
Theres an out of data library (precurser to dictionaries) that creates a dictionary. Called collections. This is slower that both sets and dictionaries
Numpy has a .unique() method but converting it to an array and back was exceptionally slow
Using a pandas series was faster than NumPy but not as fast as the in-built options
All 4 data structures removed 5757 items. This consistancy shows they are working in the same way
Looping through a for loop to check each item would be slow
Some leetcode answers suggest using pointers but leetcode isnt always the more practle in real life situations
Python lists are case sensitive, use lower() to convert all to lowercase. This removed 75 more items but reduced speed by an average of 0.0032
Removed the word 'limited' from the items in an effort to remove more items but had no effect so code was removed
Due to the above reason it is unlikely that the use of wildcards would have an impact either
Using a RegEx (regular expressions) could be an option but I would have to know what to look for and so was not used
Function only iterates once so a generator isnt necessary 

LIMITATIONS/EXTRAS
Doesnt actually check if the in-built methods are removing the same items, just assumes because they are removing the same amount
Could use a regex to find the most common letter pattens, then manually decide if that word is necessary, then remove that word from the data set
Could automate the above process?^

RESOURCES USED
https://www.w3schools.com/python/python_howto_remove_duplicates.asp
https://datagy.io/python-remove-duplicates-from-list/
https://www.programiz.com/python-programming/methods/string/casefold
https://www.geeksforgeeks.org/complexity-cheat-sheet-for-python-operations/
