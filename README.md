# Control_chart

In this mini project, I wrote a function that generates an x-bar_s control chart. The chart is based on an array with random values that are normally distributed. The array is a simulation of a process control - number of rows is number of measurements that will be displayed on the chart, and number of columns is a size of a subgroup in evey measurement. The array is generated by the function and all the parameters (mean, standard deviation, array size) are definied by the user. x_bar chart shows means of every measurements and s chart standard deviation of every measurements. The function is automated and should give a nice chart for various normal distributions and array sizes.

# Example

Here is the chart for an array of normally distributed random values, N(50,20). The array size is 25x12, which indicates that 25 measurements will be ploted, and each measurement represent a mean value (or standar deviation on the s chart) for a subgroup consisting of 12 samples. One should keep in mind that the lines visible on the plot, including the control limits (3σ), are based not on the initial standard deviation used for generating random values (20 in our case), but standard errors of all of the measurements for x-bar and s charts. Standard errors are marked as σ on the chart to stick to the convention.

<img src="control_chart.png" width="600" height="600">

The data seem to follow the normal distribution, and the simulation shows that our imaginary process is under control. There are, however, some interesing observations, that probably would catch controler's attention:
 - on the x-bar chart, from measurements 13 to 21, only 2 points are above the process mean
 - on the s chart, there is a 'hook-like' pattern for poins from measurements 5 to 11

These observations may suggest that there is a problem with a process. However, here we should remember that Python does not generate random numbers but pseudo-random numbers, therefore some unusual data patterns may occur.
