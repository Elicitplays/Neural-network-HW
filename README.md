# Neural-network-HW
 
The purpose of this analysis is to make a tool which will help the foundation determine which candidates are the best and have the highest chance of succeeding. 

# Preprocessing

When it came to preprocessing we were only concerned with the IS_SUCCESSFUL variable. We kept that as our y and then everything else as our x. When it comes to what affects this we have 4 main things, the amount requested, application type, income amount and the status. We also had features like EIN and name which got dropped. When doing the testing and grabbing the pd.getDummies() the classifiers also got dropped too. To be honest, I have no idea why.

# Compiling, Training, and Evaluating the Model

For the ideal model the parameters that were the best were an activation of tanh with the first layer having 41 neurons. Then the network as a whole has 3 layers with the number of neurons per layer being 
1. 11
2. 26
3. 21

With this we were able to achieve an acccuracy of 73.52%. It definitely isn't where we want to be as we were trying to reach above 75%. I did make 3 attempts, the first one was actually the most accurate. I had initially ran just the baseline with all the inputs/features that were aforementioned. I wanted to see whether taking some of the variables out would bring more accuracy. For the second attempt I removed the "special considerations" column to see whether it affected the accuracy. Turns out before running the tuner, the accuracy actually dropped by two percent. However after running the tuner it was brought back up to where it was with the first model with an accuracy of 73.42%. For the third try I also removed the columns that looked at special considerations, status, and the ask amount. Due to the ask amount column being dropped I also didn't have to scale the data as the rest of the data simply binary in nature. At that point the accuracy was also close to the same with it being 73.12%. With how complex this problem is this might be the best that the model could get. For more performance to be pumped out I would have to study neural networks even further than what I know currently.

# Summary

In summary, the model that has been created has an accuracy of 73.52%. This isn't the most accurate, but it could possibly help in swaying the decision whether a suitable investment can be made. Using tanh as the activation model is defintely ideal due to the noise that the data naturally produces. We could go into more epochs but that is simply using time that I do not have for this assignment. Would I reccomend using this model as the SOLE tool of determining whether a venture will be successful? No, but is it a great starting point for better models to be made? Yes
