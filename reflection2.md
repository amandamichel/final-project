# Predicting Political Elections
## A closer look into the FiveThirtyEight Presidential Forecast 

It is difficult to have any conversation now without devolving into discussions regarding the proverbial elephant (and donkey) looming over us all. Take a moment and recall what the majority of Americans believed four years ago: that, with relative certainty, Hillary Clinton would be the president-elect come November. This belief was not unfounded- the vast majority of predictive models predicted Clinton to be the clear, undisputed victor. The major predictive model that gave Trump the highest chance of winning? The FiveThirtyEight Presidential Forcast.

Nate Silver simplifies their approach to the predictive model into three major steps: taking in and adjusting polls, applying other predictive variables, and accounting for uncertaincy before simulating the election. 

FiveThirtyEight considers a specific poll by its sample size and reliability to create a weighted average of polls. This weighted average is further refined by considering predictable voters (who are not necessarily represented in polls), general biases of the polls, and change in public opinion over time. Pure polls are too suseptible to drastic, but temporary, shifts alongside major events like a party convention, scandal, or debate. So, for one to two weeks following the event, the model uses a blend of pre- and post-event polls, to prevent an extreme, unrealistic shift in the model.

To increase accuracy, the model applies demographics and voting history to the polls, then combines this with other factors (incumbancy and economy) to create the election forecast. FiveThirtyEights "partisan lean index" reflects the history of a given state; this year it gives 2016 a 75% weight and 2012 a 25% weight. This lean index is then applied to each state, alongside other variables- race, income, education, urbanization, religiosity, and COVID-19 severity- and combined with polls to create an "enhanced snapshot" of the state. Economic considerations are also made in this step, but it is not an excellent predictor because of its flexibility. In other words, the difference in economic conditions between now and election could be huge, which negatively impacts the accuracy of the model. 





*References*

Silver, Nate, [How FiveThirtyEight’s 2020 Presidential Forecast Works — And What’s Different Because Of COVID-19.](https://fivethirtyeight.com/features/how-fivethirtyeights-2020-presidential-forecast-works-and-whats-different-because-of-covid-19/) *FiveThirtyEight* (12 Aug 2020). <br/>
