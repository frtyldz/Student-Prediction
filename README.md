# Student-Prediction


You are a teacher in a secondary school and you are tasked with choosing eligible students for a special scholarship. Your school has hundreds of students and you notice that you do not have enough time to go over every student’s grades and documents to see whether they are eligible for the scholarship. Hence, you and one of your colleagues from another secondary school use your love of computer science to find a solution and decide to train a machine learning model to decide whether you should give a student the scholarship or not.
Your dataset contains answers of the survey given to students in the math course in two secondary schools from previous years [1,2]. The dataset has the following attributes. These attributes are given in the same order in the feature files as follows.
- school - student’s school (binary: ’1’ - Gabriel Pereira or ’0’ - Mousinho da Silveira)
- gender - student’s gender (binary: ’1’ - female or ’0’ - male)
- age - student’s age (numeric: from 15 to 22)
- address - student’s home address type (binary: ’1’ - urban or ’0’ - rural)
- famsize - family size (binary: ’0’ - less or equal to 3 or ’1’ - greater than 3)
- Pstatus - parent’s cohabitation status (binary: ’1’ - living together or ’0’ - apart)
- Medu - mother’s education (numeric: 0 - none, 1 - primary education (4th grade), 2 – 5th to 9th grade,
3 – secondary education or 4 – higher education)
- Fedu - father’s education (numeric: 0 - none, 1 - primary education (4th grade), 2 – 5th to 9th grade,
3 – secondary education or 4 – higher education)
- Mjob - mother’s job (one-hot encoded: ’4’ - teacher, ’3’ - health care related, ’2’ - civil services (e.g.
administrative or police), ’1’ - at home or ’0’ - other)
- Fjob - father’s job (one-hot encoded: ’4’ - teacher, ’3’ - health care related, ’2’ - civil services (e.g.
administrative or police), ’1’ - at home’ or ’0’ - other)
- reason - reason to choose this school (one-hot encoded: ’1’ - close to home, ’2’ - school reputation, ’3’
- course preference or ’0’ - other)
- guardian - student’s guardian (nominal: ’1’ - mother, ’2’ - father or ’0’ - other)
- travel time - home to school travel time (numeric: 1 - <15 min., 2 - 15 to 30 min., 3 - 30 min. to 1
hour, or 4 - >1 hour)
- studytime-weeklystudytime(numeric: 1-<2hours,2-2to5hours,3-5to10hours,or4-¿10
hours)
- failures - number of past class failures (numeric: n if 1 <= n < 3, else 4)
- school support - extra educational support (binary: ’1’ - yes or ’0’ - no)
- family support - family educational support (binary: ’1’ - yes or ’0’ - no)
- paid - extra paid classes within the course subject (binary: ’1’ - yes or ’0’ - no)
- activities - extra-curricular activities (binary: ’1’ - yes or ’0’ - no)
- nursery - attended nursery school (binary: ’1’ - yes or ’0’ - no)
- higher - wants to take higher education (binary: ’1’ - yes or ’0’ - no)
- internet - Internet access at home (binary: ’1’ - yes or ’0’ - no)
- romantic - with a romantic relationship (binary: ’1’ - yes or ’0’ - no)
3
- family relations - quality of family relationships (numeric: from 1 - very bad to 5 - excellent) - free time - free time after school (numeric: from 1 - very low to 5 - very high)
- go out - going out with friends (numeric: from 1 - very low to 5 - very high)
- Dalc - workday alcohol consumption (numeric: from 1 - very low to 5 - very high)
- Walc - weekend alcohol consumption (numeric: from 1 - very low to 5 - very high) - health - current health status (numeric: from 1 - very bad to 5 - very good)
- absences - number of school absences (numeric: from 0 to 93)
The data have been already split into two subsets: a 280-sample subset for training and a 115-sample subset for testing (consider this as your validation set and imagine there is another test set which is not given to you). You will use the following files:
• q3-train-features.csv
• q3-train-binary-labels.csv
• q3-train-multiclass-labels.csv • q3-test-features.csv
• q3-test-binary-labels.csv
• q3-test-multiclass-labels.csv
The files that end with features.csv contain the features and the files ending with labels.csv contain the ground truth labels. In the feature files, each row contains the feature vector for a student. The j-th term in the row i is the information related to j-th attribute of the i-th student. The binary-label files include the ground truth label, i.e. whether the corresponding student is eligible for the scholarship. The order of the student rows is the same in the features and the labels files. That is, the i-th row in both files corresponds to the same student’s information. You will use these files, train-binary-labels.csv and test-binary-labels.csv, for Question 3.1 and Question 3.2. The multiclass-label files include the ground truth label, i.e. whether the corresponding student is accepted, on-hold or not-eligible for the scholarship. Again, the order of the student rows is the same in the features and the labels files. You will use these files, train-multi-labels.csv and test-multiclass-labels.csv, for Question 3.3.
In this question, you will train one soft margin and one hard margin SVM classifier on the dataset explained above. You must perform 5-fold cross validation WITHOUT using any libraries but you CAN use libraries or software packages to train your SVM.
