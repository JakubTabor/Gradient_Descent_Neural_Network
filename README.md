# Gradient_Descent_Neural_Network
# I have simple dataframe, "bought_insurance" will be my "target" 
# I gonna create "Gradient Descent" from scratch and also "log loss" and activation function so "sigmoid numpy"
# First I import "train_test_split" and get "train" and "test" set, "X" will be "age, affordibility" and "y" "bought_insurance"
# Now I need to scale "age" in "train" and "test" set, so I make copy on both of them and "scale my age which is between 1 and 100"
# I create simple "Neuronal Network" with only one "output neuron" "input_shape", so my "age and affordibility", "activation is sigmoid" 
# Then "kernel_initializer", so my "weights" are initialize by "one" and "bias_initializer" by "zero" 
# Next I "compile my model" with "optimizer adam" i have binary output so "loss is binary_crossentropy" and "metrics will be accuracy"
# Then I train my model with "X_train_scaled , y_train" and number of "epochs are 5000", then I evaluate my model with "X_test_scaled, y_test"
# I check predicions and compare with real results, I also get "coefficient and intercept" using "model.get_weights()" for later comparison
# I gonna use this model to compare with my hand written model, later
# Now I write "activation function, so sigmoid", its simple function which return value in range 0 to 1, the pattern is "1/(1+math.exp(-x))"
# Then I write "prediction function", so "weigthed_sum" that I gonna use later in my "gradient descent" 
# So I write is from the pattern "coef[0] * age + coef[1] * affordability + intercept" "w1 into age + w2 into affordability + bias"
# Next I return my "weigthed_sum activated by sigmoid", then I can check some predictions 
# Now I write "log_loss" function, so I set "epsilon to very low value", then i write code for "value very close to 0" "[max(i,epsilon)for i in y_pred]"
# An next for "value very close to 1" "[min(i,1-epsilon)for i in y_pred_new]", then I put it into array "np.array(y_pred_new)"
# "-np.mean(y_true*np.log(y_pred_new)+(1-y_true)*np.log(1-y_pred_new))", now I put it into a pattern using "mean and logarithm" 
# Now I create "sigmoid_numpy", so it will return array instead of 1 value "1/(1+np.exp(-X))"
# With this helpers functions I can create "Gradient Descent function" 
