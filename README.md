# DeepLearning-Time-Series-data
Applying different deeplearning architect in time series data
This project uses different deep learning architectures to forecast multiple time series datasets. In univariate time series datasets, general statistical forecasting shows better performances, but in terms of multivariate time series datasets, different deep-learning architects can outperform statistical learning models like the ARIMA model. In today's world, there are a lot of multivariate time series data generating spontaneously, like different health data in Fitbit or Apple watch, electrical consumption under a powerhouse, etc. So, the model should be independent of seasonality, trend, and cyclability so that it can track the data themselves. It will increase the scalability of the model for multiple time series data. The motivation behind this project is to apply different probabilistic-based deep learning models in the time series dataset. Time series datasets are suitable with statistical models like ARIMA and ELS, but its hindrance is on its scalability as it is needed to track the seasonality and trend manually.  Besides, researchers are currently trying to integrate solutions to different problems in deep learning. Deep learning is easy to integrate with other AI models in plug-in and using different prepared pre-trained models. It opens the hidden strength of the data. Because of the open-source models, pre-trained models, and other researchers prepared architecture, it is easier to evaluate the model and fine tune it according to the dimension of the problem. 

Deep learning is used extensively in Natural Language Processing, image processing, and recommendation systems. It is not yet popular to apply it in time series datasets, but it has some quality to capture multiple streams of time series data, which is impossible by traditional well-established algorithms like ARIMA, AR, etc model. In 2022, Makridakis et el, did some tests to see how well different forecasting methods work (Fig-1). They picked the best two statistical methods (ETS and ARIMA) and made a combined method called Ensemble-S. They also selected the best two machine learning methods (MLP and BNN), added four new deep learning methods (DeepAR, Feed-forward, Transformer, WaveNet), and combined them into Ensemble-DL. They checked how well these methods did on an extensive set of data, using two accuracy measures (sMAPE and MASE), and also looked at how long it took for the methods to be trained and make predictions (CT) and how complex the calculations were (RCC).[1] Their tests showed that ETS and ARIMA were generally more accurate than the machine learning methods and most of the deep learning methods for all lengths of time they were trying to predict. Both the combined methods (Ensemble-S and Ensemble-DL) did better than any individual method. Ensemble-DL was slightly better overall, but Ensemble-S was the best for MASE when predicting the near future. Machine learning methods were also better than deep learning methods for predicting the near future. The researchers also found that if models are set up to be good at predicting the next immediate time point (one-step-ahead forecasting), they are more accurate for the near future. But if setting them up to be good at predicting several future points (multi-step-ahead forecasting), they do better for longer-term predictions. Statistical methods like ETS and ARIMA are usually set up to be good at the next immediate point, while machine learning methods like MLP and BNN are set up to predict several points into the future.

Traditional statistical algorithms like Exponential Smoothing and ARIMA have been staples in time series forecasting. These methods, while robust, are typically applied to individual series, requiring manual intervention to adjust for trends, seasonality, and autocorrelation. This one-size-fits-one approach struggles with scalability when dealing with today's digital world's complex, interconnected datasets—consider the vast array of product sales data at Amazon or the intricacies of user engagement metrics at Instagram. Enter deep learning (DL), a contemporary approach that flourishes with minimal assumptions, learning from the intricate relationships within massive, intertwined datasets. However, it's crucial to acknowledge that deep learning is not devoid of inherent biases—these are introduced through the architectural choices made during model design. Such biases can be advantageous, as seen with Convolutional Neural Networks (CNNs), which excel in image recognition due to their spatial biases. The selection of a deep learning model thus becomes a strategic decision that must align with the specific nuances of the application domain. With the advancement of technology, a suite of sophisticated DL models has emerged, each with unique inductive biases tailored for different forecasting challenges. This model may integrate with systems where multiple time series are parallel, for example, in Apple Watch, heart rate, daily activity data, sleep pattern, blood oxygen levels, electrocardiogram, mobility data, etc. There are multiple streams of time series data. If these time series can be integrated into one model to predict the forecast, classification, and probability distribution, it may help solve such critical health issues. Our dataset also has multiple streams; it has 370 entities of customers who are consuming energy differently, but they are sharing the same time steps at 15-minute intervals. So, the same architect can be applied to different datasets. 

We have applied different models and compared with our baseline model ARIMA.

ARIMA	1.22
Bayesian LSTM	0.82
MQRNN	0.55
DeepTCN	0.15
N-BEATs	0.06

From Table 1 and Figure 12, it can be seen that N-BEAT models show better results among all deep learning models, and among these, all the models outperform the statistical ARIMA model. So, these models and different architectures can be applied in different time series datasets. All the models have captured seasonality, trend, and cyclability by themselves, so for time series datasets, the model is scalable. So, in different applications, these models can be applied to forecast different health issues and financial forecasts. 
For future pursuing, the main focus should be divided into two sectors:
1.	Increase the robustness of the model.
2.	Detect the time complexity of the model to decrease the power and time consumption during the training periods.

   
	Increase the robustness of the model:
If these models are applied to different financial forecasts, they must be robust with noise and outliers and detect important information. Ex: Forecasting one industry cluster on a large spectrum to reduce risk management. Like, if interest rates increase, then how the financial bank will react after it?   
Some proposals can be given to increase its efficiency and make it more robust. 
•	Transformers are the proven technology for long seq-to-seq models. So, for building the model transformer can be applied to make the model for rigid and robust. 
•	There may be thousands or millions of parallel data streams can be detected where all the data streams cannot be related. To detect these relations, self-attention can be introduced when building the model.  Attention can be useful in increasing the efficiency of the model. 
•	Graph neural networks (GNN) can be applied to the model where each client can be identified as a node. And their relationship with different clients can be identified as edges. In graph neural networks, parallel time series data streams can be more connected. 
	Increase efficiency: Deep Learning models are trained in millions of data. In multiple time series datasets, it can be more important to train the model more efficiently. Flash attention, fusion method, parallelization, etc. are applied to increase the efficiency. 


These models with the architectural design are capable of forecasting in multivariable time series data. It helps different dependencies and multivariable predictors with specific requirements. It helps to make the model more precise, accurate, and robust. In general, where the system and environment become complicated and convoluted to forecast, multivariable datasets can be helpful to dictate the forecast precisely and more accurately, measuring and evaluating complete dynamics. In practical applications like finance, healthcare, or supply chain management, decisions are rarely based on a single variable. These models can be efficient in these multivariable datasets. RNN model has some limitations for gradient vanishing, and LSTM has some constraints on bottleneck when backpropagation. That’s why different convoluted autoregressive models, the N beats models or the DeepTCN models, can be helpful for forecasting. If the dataset proceeds with a million data series dataset, it can be computationally intensive to use the N beats model, but integrating attention in proper parallelization with each data stream can efficiently scale the data. Also, a Graph Neural Network may help forecast the model. In conclusion, it can be said that deep learning can be more efficient than statistical learning in multivariable datasets. 





