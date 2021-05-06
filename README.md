# Kalman-Filter
This task was assigned to me as part of the selection process for the Autonomous Ground Vehicle Research Group software team at IIT Kharagpur.
## Key Learnings
### 1. Kalman Filter - Working and Application
### 2. Plotting graphs on matplotlib
### 3. Python file handling
## Challenges and Workarounds
### 1. Storing the measurements given in the form of a matrix
The first column in the readings file has only the positions (x and y), we need to assume velx = 0 and vely = 0 in the starting. 
If I directy try to store all the lines in file in the form of a matrix, it won't work since the first row has 2 columns while the rest have 4.
So, I needed to remove the first line and store the rest in the reading matrix. For this I needed to store all the lines in form of a list. 
The first row had to be stored seperately as the initial state vector X (dim = (4,1))
### 2. Choosing matrices P, Q and R
In the 

## Scope for Improvement
## Conclusion
