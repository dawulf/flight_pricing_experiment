

## Study summary
### My study attempts to measure the effect of repeated flight price checking on the change in those prices over time.

## Scope, adjusted from proposal
In order to keep the study manageable, I have decided on the following. All flights will be limited to the basic fares of nonstop routes run by United, Delta, and American Airlines. The airports will be picked from a geographically dispersed list: SEA, SFO, LAX, DEN, DFW, ORD, ATL, BOS, and LGA. All of these airports are hubs of at least one of the three airlines of interest, and have traffic from all three. The times considered will be between 7am and 3pm on Wednesday, February 12th and Wednesday, February 19th, far enough away so that flights will not likely sell out. The websites used will be (and will be blocked on) official airline websites, as well as three independent travel sites (Expedia, Booking, and TripAdvisor).

##Assignment and treatment procedures, adjusted from proposal
I will limit the study to a control and only one type of treatment. The control will be split into halves. One will be a second experimenter located far away searching for half of the initial flight prices once. The other half of the control will be similar (same day, same single check of each price) but will be done myself, using Google Chrome’s Incognito Mode, which blocks cookies from being created. This split will allow for post-hoc analysis of any difference between the halves, and because I do not think any interaction effect exists between these halves and the particular airline or travel website used, I can combine across the latter to give more power to this analysis. 

I will randomly order a list of each route and date combination. Using complete random assignment, I will assign 1/6 to each of the three airline websites and 1/6 to each of the three travel websites. Finally, using complete random assignment, I will take each of the six equally sized groups and randomly assign 50% to potential treatment, 25% to potential control by me, and 25% to potential control by the other experimenter. The exact flight chosen will be the earliest flight within the time of interest that fits the criteria (e.g. first flight on United.com from Denver to Los Angeles between 7am and 3pm on Feb 12, first flight on booking.com from 7am and 3pm on Feb 19). Not each combination exists (especially not within the time periods of interest), and if this is the case for a combination, that selection will be skipped and the next will be looked for, effectively resulting in restricted randomization. This will continue until, for each given airline or travel website, 6 treatment units and 3 units of each type of control have their price recorded alongside the details of the particular flight chosen. Thus 36 treatment units and 36 control units will be recorded in total.

The treatment will be repeated checking (every 4 or so days) of each flight in the treatment group during the study period. During each check, I will search for flights with the intended origin and destination on the intended day on the appropriate website, then limit my search to non-stop flights and to the time period of interest on the results page. When I find the particular flight used, I will select the flight as though I was actually going to book it, stopping before I enter any personal information and exiting the page.

##Primary outcome variable
The primary outcome variable will be the percentage (relative) change in price of each flight from baseline check to final check

##Secondary outcome variable
A second variable to be calculated will be the absolute change instead of the relative change in price. This variable will be run through the same analysis as the primary outcome, but will not be used to claim a causal effect. Instead, it may provide a helpful general guideline for the scale in dollars of any effects found in the primary outcome.

A balance table will be produced showing the average price\_pre in the treatment and control group, as well as within each of the 6 website groups.

##Inclusion/Exclusion Criteria
The only reason an observation may be excluded is if the flight itself has no basic fare tickets available at the final check (or any check prior to that).

##Statistical Model and Covariates
The model will ask for the causal effect of treatment on price\_rel, while controlling with fixed effects for the website.

Other than the block fixed effects, no other covariates will be included. In effect, I expect the constructed outcome to account for much of the variability in initial price, and through that in airports, flight length, dates, and airline pricing differences, that we may have thought to include as covariates. The robust standard error generation will align the estimate of the standard errors with those we would get using the difference in means estimator. P-values will be calculated using a two-sided t-test, as we have no reason to exclude an effect in either direction.

##Subgroup Analysis
Heterogeneity is very likely should there be any effect; It is unlikely that each airline and each travel websites adjust prices based on price check history, and even less likely that they do so exactly the same amount. As a result, the exact regression above will be run separately in the halves of the data where airline\_site = 1 or 0 with $\alpha$ = 0.05/2, as well as separately at each value of the website variable with $\alpha$ = 0.05/6. Note that any use of the Bonferroni correction here is arguably unnecessary, and while I have not accounted for multiple testing across the small and intentional types of subgroups, I have chosen to include it within each subgroup analysis.

Finally, the c\_type variable will be used to compare the outcome between the two types of controls.
These should not be different, as we are assuming google chrome's incognito mode deals with the potential price adjustments we are looking for. If they are, half of the controls are not truly unaffected by treatment, and thus the validity of the entire study is at risk.