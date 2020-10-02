# Predicting Political Elections
## A closer look into the FiveThirtyEight Presidential Forecast 

It is difficult to have any conversation now without devolving into discussions regarding the proverbial elephant (and donkey) looming over us all. Take a moment and recall what the majority of Americans believed four years ago: that, with relative certainty, Hillary Clinton would be the president-elect come November. This belief was not unfounded- the vast majority of predictive models placed Clinton to be the clear, undisputed victor. The major predictive model that gave Trump the highest chance of winning? The FiveThirtyEight Presidential Forcast.

Nate Silver simplifies their approach to the predictive model into three major steps: taking in and adjusting polls, applying other predictive variables, and accounting for uncertaincy before simulating the election. 

FiveThirtyEight considers a specific poll by its sample size and reliability to create a weighted average of polls. This weighted average is further refined by considering predictable voters (who are not necessarily represented in polls), general biases of the polls, and change in public opinion over time. Pure polls are too suseptible to drastic, but temporary, shifts alongside major events like a party convention, scandal, or debate. So, for one to two weeks following the event, the model uses a blend of pre- and post-event polls, to prevent an extreme, unrealistic shift in the model.

To increase accuracy, the model applies demographics and voting history to the polls, then combines this with other factors (incumbancy and economy) to create the election forecast. FiveThirtyEights "partisan lean index" reflects the history of a given state; this year it gives 2016 a 75% weight and 2012 a 25% weight. This lean index is then applied to each state, alongside other variables- race, income, education, urbanization, religiosity, and COVID-19 severity- and combined with polls to create an "enhanced snapshot" of the state. Economic considerations are also made in this step, but it is not an excellent predictor because of its flexibility. In other words, the difference in economic conditions between now and election could be huge, which negatively impacts the accuracy of the model. 

The final considerations in this model come in the form of the uncertainty index. Large numbers of undecided and third-party voters, a wide gap between polls and other factors, economic volatility, and a large output of major new all increase the uncertainty of the model. Conversely, political polarization, stable polling, and a large volume of polls decrease the uncertainty of the model. This year, the largest contributers to uncertainty are economic volatilty and extreme volume of news output, largely due to COVID-19. The uncertainty index is then applied with varying weights for each simulation.

The model runs 40,000 simulations, applying the polls, partisan lean index, and uncertainty index at slightly different weights. They then take an average to show the likelihood of each result. As of October 1, the FiveThirtyEight Presidential Forecast places Biden's chances as 80 in 100 and Trump's at 20 in 100.

An Update as of 1:30 AM: BIDEN AND TRUMP CONTRACTING COVID-19 ISN'T IN THE UNCERTAINTY INDEX


*References*

Silver, Nate, [How FiveThirtyEight’s 2020 Presidential Forecast Works — And What’s Different Because Of COVID-19.](https://fivethirtyeight.com/features/how-fivethirtyeights-2020-presidential-forecast-works-and-whats-different-because-of-covid-19/) *FiveThirtyEight* (12 Aug 2020). <br/>
