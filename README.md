# Stock Price Forecasting with Deep Learning


## Project Overview

This repository contains all material for homework six. The main objective is to build recurrent neural networks that predict future stock prices using historical data. Two separate forecasting tasks are completed. The first reproduces a published tutorial for General Electric prices. The second creates a custom model that predicts Microsoft closing prices thirty days and three hundred sixty five days into the future.

## Repository Contents

* Main.ipynb is the main notebook that walks through every step from loading data to saving the trained models  
* ge_stock.txt holds the raw General Electric price history  
* processed_data.csv contains the cleaned Microsoft price series  
* msft_forecast.csv stores the predicted Microsoft prices  
* forecast_model_30d.h5 is the saved model for the thirty day horizon  
* forecast_model_365d.h5 is the saved model for the three hundred sixty five day horizon  
* msft_stock_model.h5 is the full Microsoft model  
* model.png shows the neural network architecture  
* stock_training.png shows the training and validation curves  

## Data

General Electric prices come from the original tutorial source. Microsoft data was collected with y finance, resampled to daily frequency, and stored in processed_data.csv for reproducibility.

## Model Architecture

Both tasks use stacked long short term memory layers followed by fully connected layers and a linear output. Mean square error is the loss function. The Adam optimizer is used with an initial learning rate of zero point zero zero one. Early stopping halts training when validation loss stops improving.

## Visual Outputs

model.png illustrates the network layout. stock_training.png compares training and validation loss across epochs. The notebook also plots actual versus predicted prices for both forecasting horizons.

## How to Run

Clone the repository. Install the libraries listed at the top of Main.ipynb. Open the notebook with Jupyter and run the cells in order. The saved h five files can be loaded with tensorflow keras load_model for inference.
