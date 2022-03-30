
Stochastic Gradient Descent and Alternating Least Squares algorithms (as described in Koren 2009)
Download starter_SGD_ALS.zip
Unzip, load mf_sgd_als_class.py into your IDE and run.

The PD-R, PD-RML100, PD-RML1M commands load data from critics, ml-100k, and ml-1m respectively. BTW, the PD prefix indicates that these are loaded as pandas matrices rather than dictionaries.

The T (Train) command generates holdout Test and Train matrices based on the original user-item dataset (using PD-R, PD-RML100, PD-RML1M). Executing this command is required before the MF-ALS and MF-SGD commands can run.

The MF-ALS and MF-SGD commands execute their respective (iterative) matrix factorization algorithm with a default set of parameters (that are changeable at run time) and report test and train MSE results at each iteration interval. A plot of results is also generated at the end of a test case run.


Sample (edited) dialog ...

PD-R(ead) critics data from file?, 
PD-RML100(ead) ml100K data from file?, 
PD-RML1M(ead) ml1M data from file?, 
T(est/train datasets?, 
MF-ALS(atrix factorization- Alternating Least Squares)? 
MF-SGD(atrix factorization- Stochastic Gradient Descent)? 
===>> pd-r

Test and Train arrays are empty!

PD-R(ead) critics data from file?, 
PD-RML100(ead) ml100K data from file?, 
PD-RML1M(ead) ml1M data from file?, 
T(est/train datasets?, 
MF-ALS(atrix factorization- Alternating Least Squares)? 
MF-SGD(atrix factorization- Stochastic Gradient Descent)? 
===>> t

Generate both test and train data? Y or y, N or n: y

Test and Train arrays are ready!

PD-R(ead) critics data from file?, 
PD-RML100(ead) ml100K data from file?, 
PD-RML1M(ead) ml1M data from file?, 
T(est/train datasets?, 
MF-ALS(atrix factorization- Alternating Least Squares)? 
MF-SGD(atrix factorization- Stochastic Gradient Descent)? 
===>> mf-als

Sample for critics .. 

ALS instance parameters:
n_factors=2, user_reg=1.00000,  item_reg=1.00000, num_iters=20

[2,1,20]

Y or y to use these parameters or Enter to modify: y

Iteration: 20
Train mse: 0.2265831984835294
Test mse: 0.6858639110217174
Elapsed train/test time 0.02 secs


PD-R(ead) critics data from file?, 
PD-RML100(ead) ml100K data from file?, 
PD-RML1M(ead) ml1M data from file?, 
T(est/train datasets?, 
MF-ALS(atrix factorization- Alternating Least Squares)? 
MF-SGD(atrix factorization- Stochastic Gradient Descent)? 
===>> mf-sgd

SGD instance parameters:
num_factors K=2, learn_rate alpha=0.07500, reg beta=0.01000, num_iters=20, sgd_random=False

[2, 0.075, 0.01, 20]

Y or y to use these parameters or Enter to modify: y

Iteration: 20
Train mse: 0.07761634315083399
Test mse: 0.6060941515470414
Elapsed train/test time 0.02 secs

PD-R(ead) critics data from file?, 
PD-RML100(ead) ml100K data from file?, 
PD-RML1M(ead) ml1M data from file?, 
T(est/train datasets?, 
MF-ALS(atrix factorization- Alternating Least Squares)? 
MF-SGD(atrix factorization- Stochastic Gradient Descent)? 
===>> 

Goodbye!

NOTE: If you want to run with a larger dataset using PD-RML1M, download and unzip the ml-1m.zip file from  https://grouplens.org/datasets/movielens/1m/ and place the unzipped ml-1m folder into the data folder along with the ml-100k folder. BTW, if you get a "codec" error opening a file containing ml-1m data, place the encoding='iso8859' parameter into the pd.read_csv() statement where the error occurred.
