---
title: "What Gets The People Going?"
date: 2022-05-10T10:19:38+02:00
draft: false
---

## An analysis of pedestrian activity in Melbourne

<!-- [Welcome our walkers](#welcome-our-walkers) -->

**Walking is universally lauded as the most efficient method of transportation of our human selves.** Walking burns calories, engages our muscles and balance and encourages healthy mindsets through brain oxidation and the intake of fresh air. It’s fast and easily maintained – there’s no need to refuel, we can get out the door and be on our way immediately.

Despite its ease of access however, pacing about is not always a comfortable experience. The obvious caveats hold. At longer distances, some sort of mechanical assistance is required, and on shorter distances we are prevented by other factors. The rain whipping in our faces, the wind beating us about – or global pandemics requiring us to maintain a healthy distance from each other and stay indoors.

And yet, walking can be wonderful. Warm sunny rays against our faces, the staggering from bar to bar in good company, the speedy anticipatory pacing towards our favourite takeaway.

So, what makes us walk? When do we decide that the trip is worth it – or perhaps, even preferable? Let us take a look.

### Welcome our walkers

To lay the foundation for this analysis, the primary dataset is comprised of over 4 million entries of pedestrian activity data collected by sensors in Melbourne’s inner city.

![Satellite image]({{< baseurl >}}/graph2.png)

<iframe src="{{< baseurl >}}/html/heat_map_loc.html"
	sandbox="allow-same-origin allow-scripts"
	width="100%"
	height="500"
	scrolling="no"
	seamless="seamless"
	frameborder="0">
</iframe>

The number of recorded pedestrians recorded over the past years follows a steady upwards pattern, with a single sharp drop in 2020 during the COVID-19 lockdowns. Despite the sharp toll taken by the lockdown, the trend maintains its upwards trajectory and one could reasonably presume that the walking activity will return to regular numbers as concerns and restrictions over the virus dissipate.

![Amount of pedestrians on street per year]({{< baseurl >}}/ped_street_total.png)

The upward trend does not seem to be the result of any actual increase in pedestrian activity; rather it is probably the result of more sensors and increased data recording.

Additionally, weekdays seem to skew towards a minor trend.

![Pedestrians on street during week all years]({{< baseurl >}}/people_week.png)

The weekday with the highest pedestrian activity is Friday, with a slight trend leading up to this day and a sharp drop the following two days. A pretty fair reasoning for this could be that Friday (and Saturday, which has slightly more activity than its fellow weekend-day Sunday) have the additional weight of nightlife activity attached to them.

An interesting pattern that does emerge from just this data, however, is the difference in weekday and weekend activity.

![Double graph of pedestrians on street during time of day, combined all years]({{< baseurl >}}/people_weekday_all.png)

Notice how across both weekdays and weekends, there is an underlying daytime—skewed curve. The weekends however have a much smoother distribution of pedestrians while the weekday plots instead have several sharp distinct peaks!

During the average week, there are four distinct spikes in the data: One at 8 o’clock, when people go to work, two peaks at 12 and 13 when people go for and leave lunch and finally one at 17 when most people leave work.

Additionally, the weekends have a slight skew towards pedestrian activity later in the evening. This is presumably Melbourne’s nightlife in action!

Pre- and post-COVID trends seem to be totally similar – the only difference being the absolute numbers are lower during the restrictions.

![Double graph of pedestrians on street during time of day, 2019]({{< baseurl >}}/people_weekday_19.png)

![Double graph of pedestrians on street during time of day, 2020]({{< baseurl >}}/people_weekday_20.png)

Do note how regardless of whether the data is from pre-COVID or post-COVID times the trends are the same - the only difference being the absolute numbers are lower during the restrictions.

There is again an underlying daytime-skewed distribution, with clear peaks in weekdays during commute and lunch hours, and a slight shift of weight towards the evening in weekends.

Another slight trend emerges if we try something different: Plotting pedestrian activity across different times of the year.

<iframe src="{{< baseurl >}}/html/heat_map_january.html"
	sandbox="allow-same-origin allow-scripts"
	width="100%"
	height="500"
	scrolling="no"
	seamless="seamless"
	frameborder="0">
</iframe>

<iframe src="{{< baseurl >}}/html/heat_map_july.html"
	sandbox="allow-same-origin allow-scripts"
	width="100%"
	height="500"
	scrolling="no"
	seamless="seamless"
	frameborder="0">
</iframe>

There is a difference, however slight, between people’s walking habits between January and July. Especially near Queen’s Cross Station and along the Bourke Street Mall, people tend to enjoy walking around more often in July. This could indicate a couple of things. First, high activity at the station, while not indicating direction, at least indicates intent – longer range travel seems to occur more often during this winter month.

Second, the increased activity in the street mall could be an indication of preference to walk during the cooler months than the hot tropical summer days of January.

But instead of speculating, why not incorporate the actual climate data and see for ourselves?

### Dancing in the rain

While differences between weekdays and weekends are to be expected (and differences between months of the year are to be anticipated), there are other factors which might influence pedestrian activity, the most obvious being weather. Crossing the pedestrian data with weather data from Melbourne in the same time periods provides for some interesting activity analysis.

The weather data has been pulled from Meteostat's Melbourne weather station from past couple of years. [Source](https://meteostat.net/en/station/94866?t=2015-01-01/2021-12-31)

There is much to say about the climate of southeastern Australia, but a quick overview is always in order:

![Sixtuple graph of avg. prec, wind and temp over past years]({{< baseurl >}}/weather_basic.png)

The trends seem quite ordinary. Precipitation is highest during the summer and in the autumn, windspeeds are mostly consistent and temperatures follow a typical clear bell curve around the summer.

Now, however, we will cross this data with the pedestrian activity of the citizens of Melbourne. Think about the topic for a moment before looking at the data: Do you think people prefer walking in clear or rainy weather? Windy or calm weather? Hot or cold?

![Combined years workdays and weekends precipitation ranges]({{< baseurl >}}/corr_perc.png)

Surprisingly precipitation seemed mostly to influence weekends where a small downward trend exists for heavier rainfall. While such correlations are not always causations (there might be hidden factors such as weather tending towards certain types at different times of the day which will coincide with people’s daily schedules), what we are seeing here seems to be a trend. The outlier of days with 8-10 mm’s of precipitation is coincidence; only few days actually had that much precipitation and coincidentally these would be days with high numbers of walkers.

Do note how the graphs have been divided into weekday and weekend trends. This is because weather seems to have less of an effect during the weekdays than during the weekends. While we can only speculate on the reason for this, one theory could be that while people are necessitated by occupational obligations to walk on the weekdays, walking on weekends is a rather voluntary activity and comfort might take a higher precedence.

![Combined years workdays and weekends wind speed ranges]({{< baseurl >}}/corr_wspd.png)

Any trends in wind-speed are harder to deduce. Weekdays could be showing a slight downward trend, but it is hard to say for sure, and the difference seems coincidental.

![Combined years workdays and weekends temperatures ranges]({{< baseurl >}}/corr_temp.png)

This might be the most surprising correlation (or rather, non-correlation!)

There exists little coincidence between temperatures and pedestrian activity, and the only indication of any potential trends are the outlying spikes resulting from bin summing. As it turns out, the only instance of correlations between pedestrians and temperatures showing any interesting observation was in 2020:

![Strange temperature graph for 2020 workdays]({{< baseurl >}}/corr_temp_wd.png)

The trends here are so skewed and irregular that the only deduction to be made is a simple one; it was a cold day in Melbourne when the lockdown was enacted!

Overall, it would seem the citizens of Melbourne do not care much about the changes in weather. They will happily pace about as they see fit, regardless of warm, cold, windy, or calm weather. Only heavy rainfall will prevent them from taking to the streets, and then, only if it is the weekend.


### Predicting pedestrians

A possible application for pedestrian-per-weather analysis is obvious: Predicting pedestrian activity based on weather forecasts! While the weather is already plenty unpredictable, meteorological science has reached a point where deductions about future climate can be made with a reasonable precision.

We thought that by teaching an artificial intelligence model on past weather patterns combined with pedestrian activity, it would be possible to induct certain patterns and theorize about these to determine how many people would walk on a given future day!

Machine learning is unpredictable however, and sometimes emergent patterns can be hard to understand. In the decision tree below, we can see which factors (temperatures, wind speeds, weekdays) have the greatest influence on making a prediction on how many people would walk on a given day. Further factors would influence the lower ‘branches’ of the decision tree but would have a lesser impact.

![Machine learning img]({{< baseurl >}}/mldraw.png)

Combined with a best effort accuracy of 35%, the model was way off in predicting pedestrian activity. That weekdays such as “Sunday” or “Thursday” would end up being the largest indicators of prediction results says a lot about how irrelevant the weather is compared to the social mechanisms in pedestrian activity.

This would however sit well with the above correlations explored; there simply is not one.
 

### Stepping off

While our findings were not as exciting as we had hoped, they are useful, nonetheless. As the predictive model shows, there is a rather lackluster correlation between the weather and pedestrian activity.

Additionally, in the direct comparisons between weather and walking trends, there is an almost total lack of trends. Only precipitation would affect our patterns, and this seemingly only in the weekends when people might have any choice about the matter. Of course, this could be useful – and sunny weather encouraging outdoor behavior is not a neglected fact. The Chinese military are known to use cloud seeding to clear the skies before parades, creating a strong framing for the show, but also carrying the side effect of bringing people outside and keeping them there.

These are all surprising facts considering the fantastical idealization of walking in the sun and the mythologized complaint about walking in bad weather. It would turn out that perhaps we as citizens in post-modern society are rather helpless subjects to the shifting ebbs of downpour and wind rather than the deciders of our paces. We are not actually deciding to walk at all. Rather these findings indicate that we walk simply when we need to. To and from commute spots, lunch breaks, between bars.

This of course extrapolates data from Melbourne to most of the western world, but we would wager similar results could be found in Copenhagen, London, and New York. Most of the time, when we are walking, we are not doing it to enjoy the sunshine – we’re probably just doing it for our next paycheck.

And perhaps it does not have to be that way. The findings here beg the question; how do people walk in other cities with vastly different climates and cultures? Is there a pattern in middle eastern countries which tropical sub-Saharan countries differ from? How does the weather influence the behavior of citizens in Singapore and Tibet? The lens of western temperate inner cities (excluding even behavior of Australians on the fringes of the cities and in the countryside) is very narrow, and there must be more interesting observations to make around the globe.

All we have got to do is go for it.



















