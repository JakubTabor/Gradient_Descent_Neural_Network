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
# First I create variables "weights"  and save them as random value "w1 = w2 = 1" and "bias variable", also "learning_rate" value here is "try and error"
# Now "length of samples", so "n = len(age)", Then I create "for loop" of my "epochs length" and put variable "weighted_sum" from "prediction_function" 
# Then "y_pred", so my "weighted_sum" activated by "sigmoid_numpy", Now I have firs part of neuron "weighted_sum and activation function"
# "loss" is my "log_loss function" which I use of "y_true and y_pred" 
# Now I gonna define "derivatives", so I take "average of sum of age and then difference of y_pred and y_true"
# Then " Next derivative", so I do this same on "affordibility", all calculation look like this "(1/n)*np.dot(np.transpose(affordibility),(y_pred-y_true))"
# Next "bias derivative", so "mean of difference of y_pred and y_true" with use of numpy "bias_d = np.mean(y_pred-y_true)"
# Now I can calculate my "weights" and "bias" "w1 = w1 - learning_rate * w1d" and "w2 = w2 - learning_rate * w2d" "bias = bias - learning_rate * bias_d"
# And I gonna print my parameters every epoch "print(f'Epoch: {1}, w1:{w1}, w2:{w2}, bias:{bias}, loss:{loss}')"
# Now I will stop my "loss" in this same point as my "tensorflow model"  "if loss<= loss_thresold: break" and I return wy weights "return w1, w2, bias"
# Now I put into my function parameters "X_train_scaled of age" and "X_train_scaled of affordibility", "y_train", number of epochs and my loss
# Finally i summon "coef and intercept" and compare my results, everything looks fine 
