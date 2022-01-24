# Channel-Formation-in-a-Candlestick-Chart

The idea was to make use of linear regression. I started by generating regression lines in the pulled data. The ends of those line segments (regression lines) would be my pivot points. To identify pivot points, I used an accuracy approach (Score of the regression model). To keep things simple I ran a loop to identify points between which I could get maximum accuracy for the regression model. My resistance and support trendlines will be parallel to the best fit regression line. Hence, in terms of the straight line equation, the only variable was the y-intercept.
Once the pivot points had been identified and I had the equations of my regression lines, I implemented a binary search (to find the respective y-intercepts) to produce resistance and support lines such that they have zero intersections with the candles. I have also introduced an error variable Epsilon that indicates the permissible length of wick intersection. Anything within the limit of Epsilon will not be considered as an intersection.
The x-axis of the plots indicates dates in the matplotlib.dates.date2num format.

Another approach:
Once pivot points had been identified, I could have started with the highest peaks/lowest troughs between a particular set of pivot points and then tried to find a line that has atmost 2 intersections (within the epsilon limit). But this would have been quite lengthy and complex. In contrast the first approach is relatively easy to implement and understand.
