# Prediction of Singapore's housing price using simple regression based models.  

This project is about the prediction of resale price of a house located in singapore, using simple regression model.   
The project struture is as follows:  
```bash
project_2      
├── code                                                                                                                
│   ├── house_EDA.ipynb                                                                                                 
│   └── house_reg_model.ipynb                                                                                                                  ├── datasets                                                                                                            
│   ├── data_dictionary_analysis.csv                                                                                    
│   ├── data_given.txt                                                                                                  
│   ├── planning_area.csv                                                                                               
│   ├── prediction_combi.csv                                                                                            
│   ├── prediction_enet.csv                                                                                             
│   ├── prediction_lasso.csv                                                                                            
│   ├── prediction_linear.csv                                                                                           
│   ├── reduced_train.csv                                                                                               
│   ├── sample_sub_reg.csv                                                                                              
│   ├── test.csv                                                                                                        
│   └── train.csv                                                                                                       
├── img                                                                                                                 
│   ├── date_dict.png                                                                                                   
│   ├── enet_res.png                                                                                                    
│   ├── goog_kurtosis.png                                                                                               
│   ├── lasso.png                                                                                                       
│   ├── lasso_res.png                                                                                                   
│   ├── lasso_vs_ridge.png                                                                                              
│   ├── least_square_sol.png                                                                                            
│   ├── lin_reg_res.png                                                                                                 
│   ├── mixed_res.png                                                                                                   
│   ├── ridge.png                                                                                                       
│   └── wiki_skewness.png                                                                                                                     ├── Project 2_slide.pdf                                                                                                 
└── README.md        
```    
---
contents  
1. [Problem Statement](#Problem-Statement)  
2. [Exploratary Data Analysis](#Data-Cleaning-and-EDA)
3. [Data](#Data)
4. [Modelling](#Preprocessing-and-Modeling)
5. [Results and Conclusions](#Results-and-Conclusions)
---
## Problem Statement  
The goal of this project is to build a regression model, using data contained in the [datasets](./datasets) folder. The model should be able to make an accurate prediction of the resale price (`resale_price`) of the house, for every house id (`Id`) that appeared in the [test set](./datasets/test.csv).  
Success will be evaluated based on common evaluation metrics such as Mean Absolute Error (MAE) and Mean Square Error (MSE), apart from scores.

Motivation:  
While this is a toy project for the purpose of learning, it shows the importance of prediction models.  
House owners who are looking to sale their property, property agents, those seeking to purchase a house, all stand to benefit from this model.  

---
## Data Cleaning and EDA  
This project is about the prediction of resale price of a house located in singapore, using simple regression model.   
This [notebook](./code/house_EDA.ipynb) covers the Exploratory Data Analysis (EDA).    
This picks out the important features that can be used to predict the flat resale price.   

---
## Preprocessing and Modeling
This note book will show the process of building regression model(s) to predict the housing price in Singapore.  
Models covered are:   
- Linear regression  
- Lasso regression  
- Ridge regression  
- Elastic Net regression  
- Combined Model  
The models are then analysed.   

---
## Data
This is [data](./datasets/) that contains the data dictionary, and all datasets and results.   

---
## Results and Conclusions
Out of all the models, the simple linear regression model have the best performance.  
The combination of models do have a lot of potential, and can probably be improved by tuning the hyper parameters, such as the weightage on different models.  
Also, the classification of models can be made better.   
For exmample, I can exclude the three room flats and shift it to the more room category.  
Otherwise, I can also try to further refine the model by flat type and location.  

The simple linear regression model is able to explain both the train and test data well.   
However, the unfortunate thing is that some factors can't be taken into account.  
Such as the direction the flat is facing, government policies and interventions.  

In conclusion, a simple linear model is able to explain most of the resale flats, by selecting the proper features.  
The R sqaured is 0.8912.  
This means that 89.12% of the variation in resale price to test set, which is not seen by model, can be explianed by the model.  
The RMSE is around $47,000.  
This means that the actual price is very likely around predicted price +/- RMSE, on average.  