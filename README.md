# The Silent Women of Hollywood
## Jennifer Wang and Alvin Zhu

Hosted on: https://6859-sp21.github.io/a4-women-in-hollywood/index.html

# Rationale for your design decisions

Our dataset provides information on whether a movie from the late 1970s to early 2010s has passed the Bechdel test. We have a temporal component and an ordinal component, thus we felt that the most natural visualization would  be a line graph that shows the percent of movies passed per year from the late 1970s to early 2010s. This line graph then serves as our base.

Because we can now take advantage of interactivity, the logical next step would then be to actually gain information about the individual movies within some specified range of years. The percentages of our line graph is a great introduction but it does not provide any details about what the movies themselves are. Thus, just for starters, we wanted to see the movie title, the release date, and whether or not that specific movie has passed the Bechdel test. To display this information, we initially thought of using a stacked bar chart where one bar is for the movies that have passed the Bechdel test and the other for those that have not, and where each individual component in the two stacks represents one movie. Stacked bar charts, however, are only interesting if the individual components of the stacks vary in size. Therefore, to introduce some variety, we thought of sizing the individual components by how much the movie grossed. This is then gives our question a new angle, one in which we can see whether the most successful movies pass or fail the Bechdel test.

However, we have quickly come into consensus how stacked barcharts are perhaps not the most aesthetic choice. Instead, we can use a packed bubble chart to convey the same information in much better visuals! This actually sacrifices the precision in displaying the total monetary grossed for all movies that pass/fail within some specified range of years and effectivenes in portraying the money grossed by going from length to area. However, neither one of those are top concerns thus the sacrifice is not too big a deal.

With the foundation of our interative visualization established, we went about adding interaction. We decided to take advantage of D3's brushing tool to help select some range of years in the line chart to display as bubbles in the packed bubbles chart. We also decided to use tooltips in the bubble chart to provide further levels of specificity that is not entirely essential to the visualization, such as the budget of the movie. 

We wanted the bubble chart to be interactive and to encourage exploration of the different movies displayed, so we made use of d3's forceSimulation functions to make the bubbles move and shift in response to being dragged and clicked. We think this small detail encourages users to play with the visualization and hover on bubbles more, therefore allowing them to see the tooltips and information about the movies. We also included buttons that would enable the user to resize the bubbles based on their budget, domestic gross, and international gross. This allows users to explore different layers of the data set more deeply.

Finally, to better create a narrative, we have added a component on our page that quickly displays if the audience's favorite childhood movie from 1973 to 2013 passes the Bechdel test. This serves to create a warm introduction between us (the visualizers) and the audience before diving into the real data visualizations. We hope that by appealing to the user's curiosity about their own movie, they will feel compelled to explore more movies that they know in the data visualization below.

## An overview of your development process

Jennifer:
* Bubble chart
* Styling
* Favorite movies form

Alvin:
* Line chart
* Brushing
* Tooltips