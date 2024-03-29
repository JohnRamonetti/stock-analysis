# Analysis of Stock Performance 2017/2018

## **Overview of Project**
### Purpose:  The purpose of this analysis was twofold.  Our primary objective was to analyze the performance of stocks based on their trading volume and annual returns for the years 2017 and 2018, and to readily ascertain what stocks performed well or poorly in those years.  The goal is ultimately to choose the most productive stocks for investment purposes.  Our secondary objective was then to increase the efficiency of the code (refactoring) so that the algorithms used herein will still be useful for much larger sets of stock data.  While the current analysis was performed on data for 12 stock tickers, the code was refactored to accomodate analysis of very large sets of ticker data.


## **Results**
### Stock Performance
#### When the analysis is run for [2017](Resources/VBA_Challenge_2017.png), it is clear that this particular group of stocks performed very well that year.  The "Returns" column lights up green, indicating positive annual returns for those stocks, with only one ticker (TERP) out of the twelve surveyed yielding a negative annual return for 2017.  For [2018](Resources/VBA_Challenge_2018.png), the analysis shows a very different result.  The annual returns are mostly in the red, with ten out of the twelve tickers showing negative annual returns.  Only 2 of the tickers had positive returns in 2018 (ENPH and RUN).  The only stocks to have positive returns for both 2017 and 2018 were tickers ENPH (+130% in 2017, +82% in 2018)  and RUN (+5.5% in 2017, +84% in 2018).
### Refactored Execution Times
#### Refactoring in this instance led to a dramatic improvement in execution times.  The original code used nested for loops that required surveying all the data once for each ticker (12 tickers requiring 12 runs through the entire set of data). In the [original nested loop code](Resources/Additional%20resources/Original_Nested_Loop_Code.png), the outer loop cycles once for each of 12 tickers, while the inner loop cycles through the entire set of annual data (3000+ rows of data).  Execution times were around 0.83 seconds for [2017](Resources/Additional%20resources/Original_Execution_Time_2017.png) and [2018](Resources/Additional%20resources/Original_Execution_Time_2018.png).  
#### The [refactored loop code](Resources/Additional%20resources/Refactored_Loop.png) utilizes only one loop through the entire set of data and stores the values of interest in a series of arrays (tickers(12), tickerVolumes(12), tickerStarterPrices(12), tickerEndingPrices(12)).  The data stored in those arrays is then output to the worksheet table with one more short (12 iteration) loop.  The efficiency of this improved algorithm reduces execution times for [2017](Resources/Additional%20resources/Refactored_Execution_Time_2017.png) and [2018](Resources/Additional%20resources/Refactored_Execution_Time_2018.png) to under 0.17 seconds.



## **Summary**
### What are the advantages or disadvantages of refactoring code?
#### While refactoring code takes time (which means money if you're paying someone to do it), it can be a valuable tool to improve the efficiency and effectiveness of your code.  It is a means of making code more adaptable, so code can be applied and utilized beyond a single use.  It should hopefully make the code cleaner and easier to follow, but also is an opportunity to find and eliminate bugs and, importantly, to make your code faster at accommplishing it's tasks.  Aside from the investment of time, there is always a risk, particularly on larger projects, of the coder introducing new problems/bugs into the code, especially if the refactoring coder is not very familiar with the original code.
### How do these pros and cons apply to refactoring the original VBA script?
#### In the current instance, refactoring took a small amount of time to yield a dramatic improvement in the execution times of our analyses.  While this doesn't seem to be a big deal when we're talking about execution times under a second, it does mean that the algorithm we've used here can now be applied to very large, real-world size sets of stock data.  When applying this algorithm to a massive set of stock data, the execution time will be appreciated.  Because this set of code is small and because the refactoring coder is very familiar with the original code, there really is no threat of disrupting the original code, or disadvantage to refactoring in this case.


________________________________
#### Contact:

#### E-mail: [john.ramonetti@gmail.com](mailto:john.ramonetti@gmail.com)
