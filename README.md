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
