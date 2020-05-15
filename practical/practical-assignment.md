# Practical assignment

**Due date: 31 May, 2020 at midnight (UTC-4).
Changes made to repositories after this time will not be considered during grading. 
Please refer to the description below for instructions on how to submit your repository.**

You have seen during class that we worry quite a lot about "p-hacking" (or the equivalent in machine learning; e.g., [see this short press article](https://venturebeat.com/2018/04/24/its-time-to-address-the-reproducibility-crisis-in-ai/)).
See for instance the 2011 [Simmons and Simonsohn](https://journals.sagepub.com/doi/full/10.1177/0956797611417632) describing how poor statistical practices can impact generated p-values.
This exercise is designed to demonstrate how researchers can (easily) produce false positives or inflated prediction rates via p-hacking.

In this assignment we are asking you to:

1. Generate a new variable (named `partY`) of random noise and add it to the existing `brainsize.csv` dataset.
 The new variable can be either continuous or categorical&mdash;you are welcome to choose whatever distribution you prefer.
1. Generate either associations with (e.g., correlations) or predictions of the new, fake `partY` variable using the existing variables in `brainsize.csv`.
   Notably, these associations or predictions _must yield_ a **significant** p-value (at the p < 0.05 threshold), but ideally the p-value should be as low as possible!
1. Generate a second, new variable (named `partY2`) using the same distribution as `partY` (but with a different random seed!) and re-run the same associations or prediction models from step (2) using this new variable as the outcome measure.

## Rules of engagement

- You will fork this repository to your GitHub account and [rename](https://help.github.com/en/github/administering-a-repository/renaming-a-repository) it to "LastName-FirstNameInitial-QLSC612" (for instance, Poline-JB-QLS612).
  All work must be done in your fork of the GitHub repository (you can, of course, clone it to your local machine to make edits).
  In order to officially submit your work you must add @jbpoline as a [collaborator](https://help.github.com/en/github/setting-up-and-managing-your-github-user-account/inviting-collaborators-to-a-personal-repository) to your fork of the repository.
- You will create a Python script (named `myanalysis.py`) that will read the `brainsize.csv` file, add the random variable (`partY`) that you want to predict or find association with, and produce results.
  - Your results should include the output(s) of the significant statistical test(s), and should include _at least_ one figure (but no more than three) demonstrating these relationships.
  - Your results should also include the output(s) of the statistical test(s) using the _second_ variable (`partY2`).
  - You are allowed to add variables to the feature / exogenous space, if desired.
- You will faithfully describe the procedure you employed to predict / find association with `partY` in a narrative write-up.
  If you would like to create a single jupyter notebook (`myanalysis.ipynb`) with code, narrative, and results intermixed you are encouraged to do so; however, you can also submit a separate Markdown/LaTeX file (`myanalysis.{md,tex}`) with your Python script.
- Your repository must _also_ contain a `README.md` file that explains how to install the necessary dependencies for your code, how to run the code, and what outputs are expected (e.g., if figures are generated what these will be called, what outputs we should see with regards to the statistical tests).
- Finally, your method must be as close as possible to a "reasonable" method.
  We leave the definition of "reasonable" here purposefully vague, but a good rule is that if the method you're applying have been widely used in the published literature on datasets of similar scale then it is likely a safe bet.

## Measures of success

- Does the history of your git repository show good organization ? Does the project respect standard organization ?
- Is your method and narrative "believable" ? That is, would it look reasonable to a naive researcher ?
- Can your code be easily run on another machine following the instructions provided ? (Tip: include a "requirements.txt")
- Does your code produce informative graphics ? (Note: please include the figures in your submission.)
- How "creative" have you been to boost your prediction / association values?

## FAQ

**Q.** "Can I work with other students in the course on my assignment?"  
**A.** You are allowed to discuss the assignment with other students but you must submit independent work.
While there can be natural similarities between submitted models, we will be checking for code duplication and cases of excessive similarity. 

**Q.** "How do I submit my assignment?"  
**A.** In order to officially submit your work you must add [@jbpoline](https://github.com/jbpoline) as a [collaborator](https://help.github.com/en/github/setting-up-and-managing-your-github-user-account/inviting-collaborators-to-a-personal-repository) to your fork of the repository.

**Q.** "Does this count towards my grade for the course?"  
**A.** Yes, this will count for 50% of your grade for the QLSC 612 course (20% is based on the first assessment on Tuesday, 12 May and 30% is based on the second assessment on Friday, 15 May).
Note, you do NOT need to complete this assignment if you are not taking the QLSC 612 course for credit (but you are welcome to do so if you'd like to practice with the skills and techniques you learned throughout the week!)

**Q.** "Can I ask TAs for help on the assignment?"  
**A.** Of course! 
You are more than welcome to ask TAs if you have questions about the assignment.
That said, we cannot guarantee the TAs will be able to answer all your questions, since the goal of the assignment is to ensure you have the opportunity to practice + develop the skills from the course.

**Q.** "Should I show all the different attempts at p-hacking I performed?"  
**A.** No!
Please only include the derived data and model that was "significant" according to the above specifications.
You should also be sure to include the check with `partY2`!

**Q.** "How should I organize my submission?"  
**A.** As long as you have the required submission files you are welcome to structure your submission however you would like (though we request nothing too complex!).
Please refer to [@emdupre](https://github.com/emdupre)'s ["Standards for project management and data organization"](https://github.com/neurodatascience/course-materials-2020/blob/master/lectures/13-may/01-standards-for-project-management/NDS2020_ShareableScience.pdf) lecture given on the 13 May for suggestions!
