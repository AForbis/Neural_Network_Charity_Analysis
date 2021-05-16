# Neural_Network_Charity_Analysis
# Overview of the analysis

    - We needed to use the features in the dataset to create a binary classifier that was capable of predicting whether charity applicants will be successful if funded by Alphabet Soup.
# Results

    - Data Preprocessing
        - The target variables were IS_SUCCESSFUL_N and IS_SUCCESSFUL_Y.
        - The variables considered to be the features of the model were all the remaining variables that were not IS_SUCCESSFUL_N, IS_SUCCESSFUL_Y, EIN, and NAME.
        - The EIN and NAME variables were neither targets nor features, and thus were removed from the input data.

    - Compiling, Training, and Evaluating the Model
        - Ultimately, in an attempt to optimize the model, I continued to add layers up until layer #6, chose the max number of neurons for layer #1 (120 - approx. 3 times the number of inputs) and then halved the neurons for each successive layer, and tried several combinations of activation functions (all relu, all sigmoid, all tanh, 1/3 of each).
        - I was not able to achieve the target model performance. All 10 steps I took to optimize the model did not result increase the model performance above 75%.
        - The 10 steps I took to try and increase model performance were: 
            - Step #1: Drop the STATUS and SPECIAL_CONSIDERATIONS columns = Failed
            - Step #2: Add 3rd hidden layer (relu) = Failed
            - Step #3: Added 100 epochs = Failed
            - Step #4: Add 4th hidden layer (relu) = Failed 
            - Step #5: Add 5th hidden layer (relu) = Failed
            - Step #6: Add 6th hidden layer (relu)= Failed
            - Step #7: Change all layers to sigmoid = Failed
            - Step #8: Change all layers to relu = Failed
            - Step #9: Change two layers to relu, two to sigmoid, and two to tanh. = Failed
            - Step #10: Change all layers to tanh = Failed
# Summary

    - The results of my final optimized model suggest that it can predict the success of the charity applicant 72.5% of the time. Though the original model at then end of deliverable 2 was virtually the same, with far fewer layers and nodes, and thus less likely to be overfitting the data. Future models might be able to solve this classification problem by collecting and incorporating additional data on the applicants that might be more impactful than some of the data we removed from the current dataset (EIN, NAME, SPECIAL_CONSIDERATIONS, STATUS). For example, an organization's history of successful projects, an organization's years of experience in the field, where the charity work is taking place, etc. 
