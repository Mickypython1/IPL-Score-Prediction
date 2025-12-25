# IPL-Score-Prediction
In the fast-paced world of IPL, where every run and decision can change the outcome of a match, predicting scores in real time has become both exciting and valuable. Deep learning, with its ability to process massive amounts of historical and live match data, is revolutionizing the way fans, analysts and even teams anticipate results. By uncovering complex patterns that humans or traditional methods might miss, deep learning offers highly accurate score forecasts, making it a powerful tool for enhancing the thrill and strategy of the game.

Implementing step by step:

# 1. Installing Libraries
We are importing all necessary Python libraries such as NumPy, Pandas, Scikit-learn, Matplotlib, Keras and Seaborn required for data handling, visualization, preprocessing and building deep learning models.
# 2. Loading the Dataset
The dataset contains data from 2008 to 2017 and contains features like venue, date, batting and bowling team, names of batsman and bowler, wickets and more. We will load the IPL cricket data from CSV files into pandas DataFrames to explore and prepare for modeling.
# 3. Exploratory Data Analysis
We will do Exploratory Data Analysis (EDA) to analyze how many unique matches have been played at each venue by counting distinct match IDs for every venue. Then, we’ll visualize this data using a horizontal bar chart to see which venues host the most matches.
# 4. Performing Label Encoding
We will convert categorical text data into numeric labels using Label Encoding because ML models work with numbers.
# 5. Performing Feature Selection
We drop date and mid columns because they are identifiers and don’t provide meaningful information for correlation analysis. By removing these irrelevant columns we focus on features that can reveal relationships useful for modeling or insights. Computing and visualizing correlations helps identify which features are related and can guide feature selection.
# 6. Splitting the Dataset into Training and Testing
We will select relevant features and the target variable then split the data into training and testing sets for model building and evaluation.
# 7. Performing Feature Scaling
We will perform Min-Max scaling on our input features to ensure all the features are on the same scale. It ensures consistent scale and improves model performance. Scaling will be done on both training and testing data using the scaling parameters.
# 8. Building the Neural Network
We will build neural network using TensorFlow and Keras for regression. After building the model we have compiled the model using the Huber Loss because of the robustness of the regression against outliers.
# 9. Training the Model
We train the model on the scaled training data for 10 epochs with a batch size of 64, validating on the test set.
# 10. Evaluating the Model
We predict scores on test data and evaluate model performance using mean absolute error (MAE).
# 11. Creating an Interactive Widget for Score Prediction
We build an interactive interface using ipywidgets so users can select match details and get a live predicted score.


