# Final Deliverables

* Executive Summary
	* For the client to ensure financial sustainability, it is crucial to maximize revenue efficiently.
	* This project aims to develop a Two-stage Direct Response Predictive Model to optimize net revenue for fundraising appeals. By leveraging machine learning, we aim to target donors effectively, balancing responsiveness and value to maximize returns.
	* Stage one utilizes classification methods to predict the likelihood of donating.



* Problem Understanding
	*The client faces the challenge of optimizing its direct-mail fundraising appeals program to maximize net revenue.
	*Traditional approaches lack precision, leading to inefficiencies. Appeal to all donors risks financial losses, while targeting only the most responsive donors neglects high-value, less responsive ones.
	*Balancing responsiveness and value are critical for success.
	*In order to generate profit, donations received must be greater than the cost of mailing the appeals. Each mail appeal costs approximately $0.80.



* Methodology: Data Analyzed
	* Demographic Data: Demographic information, donation history, and responsiveness to appeals.
	* Transactional Data: Previous campaign performance metrics, including response rates and revenue generated.
 	* Target Data: Internally collected data reflecting past donor history. Includes the target variables "TGTresp" and "TGTgiftamt" 
	* Data preprocessing
		* Cleaning the data:
			* Merged three data files using 'masterprimaryid' as the key, where each 'masterprimaryid' corresponds to a unique donor identifier. 
			* Converted currency values from string format to float data type to facilitate numerical calculations.
		* Handling missing values
			* Removed columns with missing values
				* Dropped the 'append_enviroconquintile' column due to a high proportion of missing data.
			* Removed rows with missing values
				* Removed two rows in the 'append_HomeValue' column where data was absent.
			* Replaced missing values with mean
			* Filled missing values with the mean for variables: 
				* 'append_age'; 
				* 'append_mt_OnlineInsuranceBuyer' for online insurance purchasing likelihood;
				* 'append_mt_LowDollarDonor' and 'append_mt_HighDollarDonor' for donation propensity; 
				* 'append_mt_CultureArtsEvents' for cultural event attendance likelihood. 
		* Deal with duplicate values：
			* Removed columns 'birth_year' and 'append_age_indicator' as these fields contain overlapping age information.
		* Deal with redundant values：
			* Removed 'run_date_y', 'run_date_x' columns, representing the data extraction date, and 'masterprimaryid', indicating donor IDs for their lack of contribution to predictive modeling.
	* Feature Engineering
		* Created dummy variables for following categorical variables and then dropped the corresponding raw categorical fields:
			* 'Monthly_Donor', 'YE_Behavior', 'Gift_Behavior' reflect donation timing and patterns, identifying year-end donors, regular monthly contributors, and responses to varied fundraising campaigns.
			* 'First_gift_channel', 'MRG_channel', 'HPG_channel', 'Prior_Channel_Behavior' captured the initial, most recent, highest, and preferred donation channels.
			* 'LifeCycle', 'LifeCycleDetail' ,'Donor_status' for classifying the duration of continuous donations or the time since lapse.
	* Feature selection：Use selectKbest for feature selection and review all feature distributions to find the most important features. 


* Methodology: Analytics Techniques
	* Machine Learning Algorithms: Utilizing supervised learning techniques such as logistic regression, decision trees, and ensemble methods.
	* Two-stage Model Development: Segmentation of donors based on responsiveness and gift value.
  	* Stage One:
  		* Random forest Classifier
  	* Stage Two:
  		* Decision Tree Regressor
  	 	* Random Forest Regressor	  	 	


* Results, Conclusions, and/or Recommendations

	* Stage One Results
   		* AUC:
   		
 		![image](https://github.com/DNSC-6317-GROUP8/GROUP8_Project/assets/83142814/09678756-e2f9-4558-bd3d-50897d0458a6)
   	* Stage Two Results

		* Ensembled Model Prediction vs. Actual:

   	  	![image](https://github.com/DNSC-6317-GROUP8/GROUP8_Project/assets/83142814/4c16fa56-b3de-40ef-8b89-1f1eb495625e)

   	  	* Distribution Comparison
   	 
		![image](https://github.com/DNSC-6317-GROUP8/GROUP8_Project/assets/83142814/66ab5728-cf3e-4525-a9a8-6cb6ee068626)
![image](https://github.com/DNSC-6317-GROUP8/GROUP8_Project/assets/83142814/2345c01d-5f55-4c87-882b-483032d8f352)





	* The nature of the two-stage model requires a final calculation to be made using the output from the two models. Specifically, we are  guided by the following (per donator):
		* Expected Revenue =  Probability of Donation * Predicted Gift Amount
	* Calculation Results:
		* Mean expected gift amount: $8.20
		* Max expected gift amount: $94.80
		* Interquartile range: $3.31 - $10.47



* Potential Next Steps
	* Potential actions to further optimize the direct-mail fundraising appeals program.
	* Future enhancements to the models should focus on handling outlier donors. This model’s output is limited to predicting expected gift amounts within our min and max ($0.00-$94.80). 
		* In our original training data, analysis found that outliers were gift amounts over $72.00
	* Explore integration with other fundraising channels, such as online campaigns or events.
		* Conduct further analysis on lower deciles to determine if they are more responsive to other donation channels
	* Continuously monitor and update the model to adapt to evolving donor behaviors and campaign dynamics.


* Risk Considerations
	* Over-reliance on predictive models may overlook the human element and unique donor motivations.
	* Ethical considerations regarding data privacy and transparency in model deployment.
	* Potential for unintended consequences, such as alienating donors or reducing engagement if targeting strategies are too aggressive.

 

