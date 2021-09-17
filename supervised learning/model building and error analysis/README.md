# Model Building and Error Analysis

lecture 1?

There are a few things that need to happen before we can start building the model:

Step 1: Frame the problem
- Is it supervised, unsupervised, or reinforcement learning? 
- Is it classification, regression, or something else?
- Should you use batch learning or online learning techniques?
Step 2: What does the current solution look like?
- This will provide a reference for performance, and insights for how to solve the problem
Step 3: Select a performance measure
- Root Mean Squared Error (RMSE) is common for regression and preferred for bell-curve datasets

![image](https://user-images.githubusercontent.com/89811204/132998187-34622baf-8e42-441c-80a5-d810fc90c39c.png)

- Mean Absolute Error (MAE, aka average absolute deviation) is less sensitive to outliers

![image](https://user-images.githubusercontent.com/89811204/132998292-8112443b-1107-49c8-8b9b-df909a366259.png)
- both of these measure the distance between the vector of predictiosn and the vector of target values

Step 4: Check Assumptions

Now you are ready to start coding! Check out ---- this page ---- for sample code
ch 2 intro to statistical machine learning
