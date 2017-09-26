# Stock-Market-Prediction-Machine-learning
—Machine Learning; stock prediction; Deep     Learning; styling; LSTM(Long Short Term Memory) 
 Goal Identifying the best machine learning approach for stock prediction B. Requirement This project requires gathering of stock price dataset of         S&P500Companiesfromyahoofinance.Forthispurpose,the          Pandas python module has been used.The dataset collected is         then stored as a CSV file 
III. DATASET AND TOOLS A.  Gathering Data For this project , S&P 500 list indexhavebeenused.S&P            500 has over 500 companies listed under it. Gather datasetof           all the companies and analysing correlationbetweenthemcan         serve as an important analysis for doing stock prediction.         Other leading index like Dow Jones, has comparably low         number of components which may not be efficient enough in          finding correlation of one company with another. The tool         usedforfindingcorrectionisHeatmap.Again,thecodeforthe           Heatmap was written in Python with the use of Pandas          Correlation function. B. Data Limitations
​ - The dataset gathered from Yahoo        Finance provided opening and closing prices of of eachdaya           particular company traded. The dataset had no information        about the changes in prices of stocks throughout the day.          Sometimes investors depend on the fluctuating prices       throughout the day and bid on stocks depending on the          fluctuations and volatility within a day. C.  Tools- 
​ For this project, python programming language was used. Python provides a list of scientific computational modes likes numpy, pandas, scipy and  matplotlib which are used throughout this project. Python also comes with machines learning packages like sklearn , tensorflow and keras. 
 
RESEARCH METHODOLOGY A.    Getting S&P 500 Tickers- 
​ The S&P 500 list is available in wikipedia and a python script was written to crawl the wikipedia page of S&P 500 list and gather all the names of companies listed in it. Dta was gathered using BeautifulSoup module provided by python. All the names of companies were stored in a pickle file. B.    Getting data from Yahoo Finance- 
​ The pickle file was loaded. A for loop was run for every ticker in the pickle file and pandas module was used to get stock data associated with every ticker. For each ticker, a corresponding CSV file was generated and stored in the working directory. Each CSV file contained open, high, low and close columns. 
 
C.    Data Visualisation- 
​ A CSV file was generated, containing only the closing prices of all the companies.Closing prices of all the companies was later visualised to form a Heat Map. The heatmap showed how a company is related to all other companies. The relation a can be positively related,negatively related and neutral. All these relations are denoted by different colors in the heatmap. For an instance, a company which is related positively to other companies would mean that if stock prices of other companies increases then, the stock price of the positively related company also increases and vice versa.  
 
D.    Applying Machine Learning- 
​ Before applying machine learning, the CSV file containing the closing prices of all the companies needed to be modified. In order to train the machine learning classifier to look into the future , the training 
and testing data should be available in a similar format. Therefore the closing price column had to be shifted back by “n” days and a new column in formed highlighting the shifted price. There are two ways in which machine learning can be applied. 1).    Time Series Prediction with deep learning Keras- Time series analysis is a way of analysing the time series data in order to extract feature-sets of the data.Keras is a high-level neural networks API, written in Python and capable of running on top of either TensorFlow or Theano. It was developed with a focus on enabling fast experimentation. The time series prediction problem can be rephrased as regression problem, that is- given the stock [price of the present day, what will be the stock price of the next day. Initially , the CSV file contained a single column data. But, using simple functions it can be converted into a two column dataset. The first column containing the present day's stock price, and the second column containing the next days stock price which needs to be predicted.This project has working SciPy environment with the Keras deep learning library installed. ● First, modelling of the data is important. Now, the accuracy of the model is checked on the training dataset. Inorder to make the model work for unseen data, training is essential. ● The dataset is splitted in training and testing dataset in 60:40 ratio. However , the ratio can be adjusted so as to observe the accuracy of the model under different ratios. ● The training and testing datasets are numpy arrays. Each array consists of two lists, dataX and dataY. ● dataX can be mapped to dataY by passing the dataset through Multilayer Perceptron Model. ● Various parameters need to be specified likethe number of hidden layers,neurons present in each hidden layer, the output layer and input layer.Stacking of layers can be simply done by the .add() method provided by keras ● configure the learning process using  .compile() method provide by keras. Keras provides an easy way to configure the optimizer. ● The cost function for the model is mean squared error. The training data is iterated in Batches ● Evaluate the performance of the model using .evaluate() method. ● The data is plotted showing the original dataset as blue and the predicted dataset as red  