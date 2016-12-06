
# brainwave-svm-cross-validation
From https://github.com/jijames/brainwave-svm-login, I test throught Cross-validation using Svm. Each person has 9 Experiments data and I make models like this:

A 1 2 3 4 5 6 7 8 9
B 1 2 3 4 5 6 7 8 9
C 1 2 3 4 5 6 7 8 9

First, I make model except Person A-1 experiment.. and Try this 9 times per one Person. ("train.sh")

so Model made like this.
A_except1, A_except2, ....., A_except9
B_except2, .... C_except9

Second, I predicted each tests by each models.(9*9 times) This is coded in "predict.sh"

The result like this.

기범_test.기범_model Average =  0.0739279
원석_test.기범_model Average =  -0.162976
태환_test.기범_model Average =  -0.0334192

기범_test.원석_model Average =  0.0437607
원석_test.원석_model Average =  0.168315
태환_test.원석_model Average =  0.0210761

기범_test.태환_model Average =  -0.0584809
원석_test.태환_model Average =  0.103501
태환_test.태환_model Average =  -0.00806665

Near to -1 mean is different to each one. Near to 1 mean is same to each one

But I think it has a large range Accuracy. Maybe DataSet is not good enough..:'(
