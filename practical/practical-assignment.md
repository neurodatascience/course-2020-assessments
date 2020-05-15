# Practical assignment

You have seen during the class that we worry quite a lot on what is called "p-hacking", or the equivalent in machine learning [see this short press article](https://venturebeat.com/2018/04/24/its-time-to-address-the-reproducibility-crisis-in-ai/) or many others. In their seminal 2011 article, Simmons and Simonsohn describe how bad statistical practice can impact p-value.  

This exercise is designed to make you realize how we can produce false positives or inflated prediction rates. We are asking you to take the brain size data in the repository, add a column of random noise (you are welcome to choose the distribution), and make either a continuous or a categorical variable that you will need to predict, or find association with the variables in the "brainsize" data. The new variable will be called "partY". 

Rules of engagement:
- You will create a python program (myanalysis.py) that will read the csv as input, add the random variable (partY) that we want to predict or find association with, and produce the results (including at least a figure, at maximum 3 figures). You are allowed to add some variables in the feature / exogenous space. 
- Your method must be as close as possible to a "reasonable" method.
- You will describe faithfully the procedure you employed to predict / find association with partY in a "narrative" section. Code and narrative can be included in one jupyter notebook but you can also have a markdown/latex file and a .py file. 
- You will submit your assignment by sending me an invite to collaborate to your GitHub repository. Please name your repository "LastName-Initials-QLS612" (for instance, for me: Poline-JB-QLS612)
- Your repository must contain a README.md that will explain how to launch the code and what is expected as a result. 

Measure of success: 
- how "creative"  have you been to boost your prediction / association values?
- is the history of your git repository showing a good organization ? is the project respecting standard organization ?
- is your method narrative "believable" ?
- is your code run easily on another machine ? (tip: include a "requirements.txt")
- did you produce informative graphics ? 

You can finish the assignment by re-generating randomly a new "partY" and see what is the new association or performance with the new variable and the brainsize data.
