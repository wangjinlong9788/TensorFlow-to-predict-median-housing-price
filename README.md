# TensorFlow to predict median housing price



Learning Objectives:

Use the LinearRegressor class in TensorFlow to predict median housing price, at the granularity of city blocks, based on one input feature

Evaluate the accuracy of a model's predictions using Root Mean Squared Error (RMSE)

Improve the accuracy of a model by tuning its hyperparameters

# LinearRegressor process

 

# 1 define
linear_regressor = tf.estimator.LinearRegressor(
    feature_columns=feature_columns,  
    optimizer=my_optimizer   )
 
# 2 train
linear_regressor.train(
    input_fn=lambda: my_input_fn(my_feature, targets),  
    steps=100  )
 

# predict
predictions = linear_regressor.predict(
    input_fn=lambda: my_input_fn(my_feature, targets, num_epochs=1, shuffle=False)
)
 


