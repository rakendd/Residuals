# Residuals
In Computational Fluid Dynamics simulations, to conclude whether the simulation is converged or not, we usually look at the residual values. <br>
Looking at the Force plot residual, if the plot has reached a stabilized state (values flatlined), we can conclude simulation has converged, i.e. there won't be any change in averaged flow field with time. 
For unsteady case, Since this is unstedy flow case, the residual plot of Total force will be oscillating around an average value. 
But this entire oscillation will be settling down with the timesteps. 
This is python code to check the residual plot if it has reached that stabilized state. 
After ommiting initial transient stage and considered last time steps for this plot. 
For this used Numpy polyfit(x,y,deg) function for finding best fit of polynomial of degree 'deg' to a set of data points given by the array of arguments x and y. 
Also used utility poly1d to plot the above found polynomial. 
