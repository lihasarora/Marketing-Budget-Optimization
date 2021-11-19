# Marketing Budget Optimization
RM 294 – Optimization I 
Project 1 – Linear Programming

Deliverables
One well-written pdf file and one Python code file (.py or .ipynb), submitted to Canvas. Your report should go into some detail about how you solved the problem, include some graphs that explain your results, and include relevant code chunks in the final output. Your report can be created by taking screenshots of the code/graph and assembling it in a word document, then export as a pdf file. 


Problem Description
Marketing budgets now comprise 11 percent of total company budgets, based on a CMO survey sponsored by the Fuqua School of Business at Duke University, Deloitte LLP, and the American Marketing Association. However, the effectiveness of marketing varies significantly: on the one hand, P&G cut more than $100 million in digital marketing spending because their digital ads were largely ineffective; on the other hand, Netflix plans a 54% boost in ad spending because they got very positive feedback in international markets.

One potential reason for such variation is the way of making marketing budget allocations. Namely, how much to invest in each advertisement platform. As stated in the Handbook of Marketing Analytics:

...budget decisions are often based on gut feelings or on the negotiation skills of individual managers. Consequently, politics and individual opinions tend to shape the decision process instead of fact-based discussions. Obviously, these rules and practices bear the risk of results far away from the optimal, profit-maximizing budget.

Indeed, the marketing strategy of Netflix seems to be steered by data. 

In this project, we use linear programming to build a simple marketing budget allocation strategy.
Specifics
1)	Assume that your company is deciding how to spend a marketing budget of $10M.  You work in the marketing department as a data scientist and the chief marketing officer has asked you write a report recommending how to spread this budget among several marketing mediums.  Your department has employed an outside consulting firm to estimate the return on investment (ROI) of each marketing medium under consideration.  The results are in the table below, and also in a CSV attached to this assignment:
 
2)	On top of these ROIs, your boss has decided to constrain your budget as follows:
a.	The amount invested in print and TV should be no more than the amount spent on Facebook and Email. Surprisingly, email seems to be a great channel for reaching real people.
b.	The total amount used in social media (Facebook, LinkedIn, Instagram, Snapchat, and Twitter) should be at least twice of SEO and AdWords.
c.	For each platform, the amount invested should be no more than $3M.
3)	Formulate the marketing budget allocation problem as a linear program.  Use gurobi to find the optimal budget allocation.
4)	Your boss is happy to see the promising results presented by the marketing department. However, your boss is also very concerned because your boss recalls being somewhat disappointed after following such recommendations in the past. To be cautious about the decision, your team has decided to get another opinion about the ROI data and rerun the analysis.  The second consulting firm returns the estimates of the ROI data in the table below (also in the CSV file mentioned above).  You are asked to compare the two optimal allocations from these two ROI estimates.  
 
5)	Are the allocations the same?  Assuming the first ROI data is correct, if you were to use the second allocation (the allocation that assumed the second ROI data was correct) how much lower would the objective be relative to the optimal objective (the one that uses the first ROI data and the first allocation)?  Assuming the second ROI data is correct, if you used the first allocation how much lower would the objective be relative to the optimal objective?  Do you think the third constraint above, based on your boss’ experience, is useful?
6)	To explore this further perform some analysis of how your optimal allocation would change based on changes in the ROI data.  Use the first ROI data as your starting point.  By how much could each advertising medium’s ROI increase or decrease and still result in the same optimal allocation you found in step (3)?
7)	Your boss has gained permission to reinvest half of the return. For example, if the marketing obtains a 4% return in January, the budget of February will be $10M + $10M × 4% × 50% = $10.2M.  The monthly ROI for next year is given in Project1.Rdata. The three constraints given by your boss are still in place for each month.  What is the optimal allocation for each month?
8)	A stable budget is defined as a monthly allocation such that for each platform the monthly change in spend is no more than $1M. Is the allocation you found stable? If it isn’t, you do not need to solve a new optimization model.  Describe how my might model this?
9)	Write an pdf file that does all of this and summarizes your analysis with graphs, text, and code chunks. The first few lines of the Rmd file, in the first code chunk at the beginning, should include pd.read_csv call that reads the csv file that has the ROI data.  Be sure to include a noticeable comment that lets us know where you read the csv files.  The template csv files fit the correct format.  To be graded, we will change this pd.read_csv call to load a new csv file and re-run your code to see if you get the right answer on new data.  Failure to run will automatically reduce your grade by 10 percentage points!  Be sure that all your analysis in the python code file is generalized, so when we load the new csv files the output will be for the new data, instead of the template data.  That means you should not hard code any numbers.  Instead you should reference variable names for your output.  
10)	Grading will be based 66% on whether you get the right answer or not when we re-run your analysis with new data.  If you don’t get the right answer or your python code file doesn’t run, we will go through your code and give partial credit accordingly.  The easier it is to read your code the easier it is for us to understand what you’re doing, so use a lot of comments in your code! The remaining 34% of your grade is based on the quality of your analysis and presentation of results in the pdf file.
