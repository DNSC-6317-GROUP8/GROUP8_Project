# Final Deliverables

* Executive Summary
	* For the client to ensure financial sustainability, it is crucial to maximize revenue efficiently.
	* Mention the approach and aim taken to develop a two-stage direct response model: This project aims to develop a Two-stage Direct Response Predictive Model to optimize net revenue for fundraising appeals. By leveraging machine learning, we aim to target donors effectively, balancing responsiveness and value to maximize returns.
 	* Stage one utilizes classification methods to predict the likelihood of donating.
  	* Stage two performs regression analysis to predict gift amount. 


* Problem Understanding
	* The client faces the challenge of optimizing its direct-mail fundraising appeals program to maximize net revenue. 
	* Traditional approaches lack precision, leading to inefficiencies. Appeal to all donors risks financial losses, while targeting only the most responsive donors neglects high-value, less responsive ones. 
	* Balancing responsiveness and value are critical for success.
 	* In order to generate profit, donations received must be greater than the cost of mailing the appeals. Each mail appeal costs approximately $0.80. 


* Methodology: Data Analyzed
	* Demographic Data: Demographic information, donation history, and responsiveness to appeals.
	* Transactional Data: Previous campaign performance metrics, including response rates and revenue generated.
	* Data preprocessing includes cleaning, normalization, and feature engineering to prepare for analysis.


* Methodology: Analytics Techniques
	* Machine Learning Algorithms: Utilizing supervised learning techniques such as logistic regression, decision trees, and ensemble methods.
	* Two-stage Model Development: Segmentation of donors based on responsiveness and gift value.
  	* Stage One:
  		* Decision Tree Classifier
  	 	* Logistic Regression
  	* Stage Two:
  		* Decision Tree Regressor
  	 	* Random Forest Regressor	  	 	


* Results, Conclusions, and/or Recommendations

	* Stage One Results
   		* AUC:
   
 		![image](https://github.com/DNSC-6317-GROUP8/GROUP8_Project/assets/83142814/bb86973e-f493-49de-b5aa-3b670fc8427b)
   	* Stage Two Results
  
   	  	* Residuals:
   	  
  		![image](https://github.com/DNSC-6317-GROUP8/GROUP8_Project/assets/83142814/259f2b1b-e9a4-4fda-8cde-9e1dab00bfd4) ![image](https://github.com/DNSC-6317-GROUP8/GROUP8_Project/assets/83142814/c3585659-a000-4349-9ef7-5c7a70ba8082)

		* Ensembled Model Prediction vs. Actual:

   	  	![image](https://github.com/DNSC-6317-GROUP8/GROUP8_Project/assets/83142814/25b113a1-6a54-4549-97dc-ed2aef5d8daf)

   	  	* Distribution Comparison
   	 
		![image](https://github.com/DNSC-6317-GROUP8/GROUP8_Project/assets/83142814/0482fcd0-20c8-431d-9c69-83bda49f1ddc) ![image](https://github.com/DNSC-6317-GROUP8/GROUP8_Project/assets/83142814/875de3ca-dd07-433e-9331-246d59cbebd8)




	* The nature of the two-stage model requires a final calculation to be made using the output from the two models. Specifically, we are  guided by the following (per donator):
		* Expected Revenue =  Probability of Donation * Predicted Gift Amount
	* The key findings or insights gained from the analysis.
	* Conclusions drawn and recommendations for future campaign strategies.


* Potential Next Steps
	* Potential actions to further optimize the direct-mail fundraising appeals program.
	* The future developments or enhancements to the predictive model.
	* Explore integration with other fundraising channels, such as online campaigns or events.
	* Continuously monitor and update the model to adapt to evolving donor behaviors and campaign dynamics.


* Risk Considerations
	* Over-reliance on predictive models may overlook the human element and unique donor motivations.
	* Ethical considerations regarding data privacy and transparency in model deployment.
	* Potential for unintended consequences, such as alienating donors or reducing engagement if targeting strategies are too aggressive.

 

