# Estimated Time Arrival using Long Short Term Memory

## Project Objective
Uncertain ship arrival time estimates can result in distribution delays, additional costs and decreased efficiency, therefore a solution is needed in the form of ship arrival time predictions with the hope of increasing the accuracy of ship arrival times so as to increase efficiency.

## Dataset and Src
- <a href="https://github.com/Nathasyarnt/Estimated-time-Arrival-using-Long-Short-Term-Memory/blob/main/Data.zip">Dataset</a>
- <a href="https://github.com/Nathasyarnt/Estimated-time-Arrival-using-Long-Short-Term-Memory/tree/main/Src">Src</a>

## Process
- Collecting AIS ship data sourced from Jorf Lasfar Port, Morocco
- Data exploration to understand the data structure used.
- Pre-processing of AIS data including data cleaning, data transformation, and creation of designed features carried out as follows:

  a. Selecting variables that are in accordance with the research objectives.

  b. Selecting ships heading to the specified port.

  c. Deleting ship journeys that have not sent AIS signals for more than 1 day.

  d. Transforming the actual ship direction into the actual steering direction relative to the north and south poles using the trigonometric functions sin and cos.

  e. Deleting AIS messages with unrealistic speeds, namely SOG ≥ 20 knots.

- Creating the infrastructure of the LSTM machine learning model

  a. Selecting input and output features or variables.

  b. Building an LSTM model with the best hyperparameters.

- Divide the data into 50% train data, 25% valid data and 25% test data using the holdout validation method to maintain the data sequence.
- The process of forming the LSTM model.

  a. Training the LSTM model with AIS data variables and designed features into the LSTM model infrastructure with the best hyperparameters.

  b. Validating the suitability of the model to see indications of underfitting or overfitting. If underfitting or overfitting occurs in the model, it means that the model is not suitable, then fine tuning of the hyperparameters will be carried out on the model infrastructure. If this does not happen, it will continue to the next research stage.
- Conducting model testing on the hybrid LSTM model to determine the error in predicting the estimated ship arrival time.
- Conducting model evaluation and interpretation of results.
- Drawing conclusions and suggestions.

## Project Result
- <a href="https://github.com/Nathasyarnt/Estimated-time-Arrival-using-Long-Short-Term-Memory/blob/main/Result.zip">Result</a>
