**This function estimates a linear regression with time-varying coefficients** 

It has the following arguments:

*dependent variable*: Enter the name of the time series 

*regressors*:  Create a list of names of the regressors.

*vector of variance ratios*: A vector of variance ratios in the form
{*r1,r2,... rn*} - one ratio for each regressor in the list of regressors. 

If a variance ratio is positive, iteration starts with this value; if it is zero, the respective coefficient is taken as time-invariant; if it is negative, its absolute value determines the fixed variance ratio for the respective regressor. 

The default is *[auto]* - the coefficients for all regressors are taken as time-varying. Their variance ratios (which reflect their variability) are estimated, and all initial variance ratios are taken as *1*.

*plot result*: If this checkbox is checked, the result is plotted. This requires that the function package TVCplots is installed. 

-If not installed, go to Gretl's main window and select *Files -> Function packages -> on server -> TVCplots*, right-click on "Install" and confirm menu attachment.

-If installed, go to Gretl's main window and select *View -> Multiple Graphs -> Time series with confidence bands (TVC)* to configure plot appearance.
  
*likelihood estimation instead of moments estimation*: If this checkbox is checked, likelihood estimation rather than moments estimation will be performed. (Not recommended.)
