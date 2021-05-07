# Kalman-Filter
This task was assigned to me as part of the selection process for the Autonomous Ground Vehicle Research Group software team at IIT Kharagpur.
## Key Learnings
<p> 1. Kalman Filter - Working and Application </p>
<p> 2. Plotting graphs on matplotlib </p>
<p> 3. Python file handling </p>

## Challenges and Workarounds
### 1. Storing the measurements given in the form of a matrix
The first column in the readings file has only the positions (x and y), we need to assume velx = 0 and vely = 0 in the starting. 
If I directy try to store all the lines in file in the form of a matrix, it won't work since the first row has 2 columns while the rest have 4.
So, I needed to remove the first line and store the rest in the reading matrix. For this I needed to store all the lines in form of a list. 
The first row had to be stored seperately by appending [0, 0] as the initial state vector X (dim = (4,1)).
### 2. Choosing matrices P, Q and R
In the task, we were asked to choose the state covariance matrix (P), noise covariance matrix (Q), and measurement error matrix (R) on our own. 
Since, the state covariance matrix is constantly updated according to the Kalman Filtering Algorithm, it's initialisation won't affect the results much. 
The covariance matrix is taken as diagonal based on the assumption that the position and velocity measurements have no co-relation, so covariance = 0. 
However, Q and R must be chosen carefully. The approach I took to solve this challenge was to plot the predicted measurements as well as the actual measurements using matplotlib. 
I tuned the values of Q and R (both diagonal matrices) until the predicted measurements graph had the same shape as that of the actual measurements, but with lesser noise. 

## Scope for Improvement
### 1. A proper approach to choose Q and R 
Rather than using hit and trial, a better method could be adopted to logically choose Q and R matrices.
## Conclusion
Overall, the coding part of this task was not heavy compared to the other tasks. However, I really enjoyed learning about the Kalman filter via this task.
