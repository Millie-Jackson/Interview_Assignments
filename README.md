# Interview_Assignments
Various task solutions from interviews. Inludes thought processes and discussion

XAPIEN

TASK

Background: Every time one of our users runs a report our Search & NLP pipeline fetches loads of information about them from company records, news articles, and blog posts. After completing this it will be able to generate a list of all company names it’s seen, we want to deduplicate entries in this list, so that our Report Generation pipeline can group together information about the same company before displaying it to the user.
Task: Write a function which takes in a list of company/organisation names, and reduces the list to one entry per company. Lots of companies will be in their multiple times, possibly with different forms of their names. The file provided should be treated as a representative example of the list of names your function will receive. You should carefully consider the time complexity of your code.
Include unit tests to show that your function works on various edge cases. The problem is fairly ill-defined and open ended, so part of the challenge is to define some bounds for your work! We're not looking for a complete solution - just a decent stab, a few good ideas and some sensible code.
Feel free to import and use any libraries or external datasets you like - that's a key part of real-world software development.
You should take care to ensure your code is readable and well-commented where necessary. Share your code (the whole solution, including the tests) with us (zip in an email, or public GitHub project). Please also share with us any additional comments, thoughts, or ideas about any difficulties you encountered in this task, and please take care to explain any limitations of your solution which you're aware of.

SOLUTION
