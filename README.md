# Football-Predictor
The project retrieves data from one API and one free database. This data is then preprocessed and finally applied in an AI model that tries to predict the outcome of the matches as well as the best bets and their sizes.  


Problems: 

	Over time, I had to recreate many times the data retrieved and the pipeline used. 
	In the beginning, it was due to a lack of practice and knowledge in the area. 
	However, the lack of information was and is a big obstacle, that lead me to rethink and recreate the entire project many times.
	
	The biggest obstacle so far is the variance compared with the dataset achieved. 
	Many large adjustments were made to extend the training dataset, by expanding the data retrieved and imputation of missing values.

Tunning:

	Model Tunning: Logistic Regression, Decision Trees, Random Forests, LightGBM classifier, NN, customized NN,
	ensemble methods.
	
	Betting Tunning: Hyperparemeters were created to handle bet sizes, betting types, and betting thresholds 
	
Project - Folders and Files:

	0 - Database: holds the data 
	1 - Get_Data: holds python scripts responsible for obtaining data from API and open database 

	2 - Pipeline
		Model: holds models architecture and execution 
	
		Preprocess: holds preprocessing of data, so it's prepared to be applied to models
	
		Score: holds functions that output the prediction quality given by an  expected profit 
	
		Pipeline: scripts that work as a pipeline, connecting all these steps.
			Allows:
				Tunning of Models
				Tunning of Model to predict odds of games with no odds 
				Training the Optimized Model
				Training the Model and create Stats - Model Analyses
				Predict Future Games 
		
	
	3 - Execute Pipelines: scripts that execute those possible functionalities given by the pipeline 

	4 - Model Analyses
		Best Within: finds best Betting Hyperparemeters within each Tunned Model Combo 
	
		Check_Consistency: retrain tunned models, to get an average of the model predicting quality 
	
		Check_Tunning: compares the different model combos, by using an  average performance on the multiple betting combos 
	
		Stats: provides plots and statistics on the performance of subdivisions in specific data features
