# TeradataUniversityNetworkDataChallenge2017

  Of all the projects I've done, the project completed using Rise Against Hunger's Salesforce data was by far my favorite. It was my first opportunity to perform every role in a full-lifecycle analytics project: data acquisition, cleaning and transformation, modeling, write up, and presentation. 

  By performing every role myself, I finally learned the nuances of each stage of the process, struggled with the variety of potential solutions, and identified insights that were uniquely my own. That the data was by far the dirtiest and largest I've played with so far was a bonus.

  The following is code for the 2017 Teradata University Network's Data Challenge (Rise Against Hunger Salesforce data). Rise Against Hunger provided three data sets and one data definition file: Accounts (258 variables, 233274 observations), Contacts (188 variables, 262201 observations), Opportunities (356 variables, 142201 observations), and a Salesforce data dictionary. 
  
  I set as the initial objective identification of the most significant predictors of donor giving (Total_Giving), which I later revised to significant predictors of a battery of criterion variables (e.g. inkind giving, events, total meals, etc.). The final model exluded the Opportunities data set: Accounts and Contacts contained cross-sectional data and Opportunities contained panel data. Accounts and Contacts were merged based on the Id == AccountId variables.

  RAH provided broad guidelines for the project that focused on donor engagement and retention. With those broad guidelines in mind, I pursued the single objective of identifying cross-sectional donor preference variables that reflected the highest beta coefficients for (initially) total giving and (later) a battery of criterion variables. 
  
  Using 41 donor preference variables as predictors, each criterion variable was estimated using partial least squares regression. From these regressions, beta coefficients were drawn from each criterion variable's predictors. The top 20 beta coefficients were consolidated for each regression, yielding a robust measure (across criterion variables) of predictor variable importance. Due to time constraints, the list of important variables was not ranked. Instead, predictors with high beta coefficients were presented as an aggregate that identified last Annual_Report_Subscriber, MP_Event_Host, Do_Not_Mail, Do_Not_Call, and HasOptedOutofEmail among the most common high beta coefficient variables.
  
  The findings suggests that among the primary drivers of donor giving (in terms of time, money, and inkind donations) is willingness to engage with RAH communications, implying that RAH should focus its resources on providing the most effective and targeted content via newsletter, email, and phone to potential donors. Highly targeted marketing content may be the most effective means of engaging donors across several types of giving.
