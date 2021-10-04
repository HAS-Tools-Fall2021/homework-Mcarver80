### **Monique Carver**
**Assignment 6**

**10/04/2021**

### **Python Code and Explanation:**

My forecast streamflow predictions for this week were based on the plots that I created. 


#1 

This plot shows the daily average stremflow (in cfs) from the year 1989-2021.

    fig, ax = plt.subplots()
    ax.plot(data['datetime'], data['flow'], color='yellow',
            linestyle='solid', label='daily')
    ax.set(title="Observed Flow", xlabel="Date", 
            ylabel="Daily Avg Flow [cfs]",
            yscale='log')
    ax.legend()

    fig.set_size_inches(5,3)
    fig.savefig("Observed_Flow#1.png")


#2

This plot has more length and displays the weekly average flow (in cfs) for the year of 2018 and the month of October.

    fig, ax = plt.subplots()
    ax.plot(data['datetime'], data['flow'], label='flow',color='green')
    ax.set(title="Observed Flow", xlabel="Date", ylabel="Weekly Avg Flow [cfs]",
            yscale='log', xlim=[datetime.date(2018, 10, 1), datetime.date(2018, 10, 30)])
    ax.legend()
    plt.show()

    fig.set_size_inches(10,3)
    fig.savefig("Observed_Flow#2.png")

#3

This is a scatter plot that displays the average flows in October 2018 vs. the average flows of 2020.

    fig, ax = plt.subplots()

    ax.scatter(data[(data['year'] == 2018) & (data['month'] == 10)].flow,  data[(data['year'] == 2020) & (data['month'] == 10)].flow, marker='p',
            color='red')
    ax.set(xlabel='2018 flow', ylabel='2020 flow', yscale='log', xscale='log')
    ax.legend()

    fig.set_size_inches(10,3)
    fig.savefig("Observed_Flow#3.png")


#4

This is the creation of two histograms that compare the month of September vs. October in log. 

    fig, ax = plt.subplots(1,2)

    m = 9
    month_data = data[data['month'] == m]
    plot_title = 'Month ' + str(m)
    ax[0].hist(np.log10(month_data['flow']), bins=30, edgecolor='grey', color='limegreen')
    ax[0].set(xlabel='Log Flow cfs', ylabel='count', title=plot_title)

    m=10
    month_data = data[data['month'] == m]
    plot_title = 'Month ' + str(m)
    ax[1].hist(np.log10(month_data['flow']), bins=30,
            edgecolor='grey', color='violet')
    ax[1].set(xlabel='Log Flow cfs', ylabel='count', title= plot_title)
    plt.show()

    fig.set_size_inches(5,3)
    fig.savefig("Observed_Flow#4.png")

#5

This plot uses a dotted line representing the daily streamflow data (in cfs) from 1989-2021.

    fig, ax = plt.subplots()
    ax.plot(data['datetime'], data['flow'], color='skyblue',
            linestyle=":", label='daily')
    ax.set(title="Observed Flow", xlabel="Years", 
            ylabel="Daily Avg Flow [cfs]",
            yscale='log')
    ax.legend()

    fig.set_size_inches(10,3)
    fig.savefig("Observed_Flow#5.png")


#6

This plot measures the weekly average streamflow (in cfs) for the month of October in the year of 2003.

    fig, ax = plt.subplots()
    ax.plot(data['datetime'], data['flow'], label='flow',color='hotpink')
    ax.set(title="Observed Flow", xlabel="Date", ylabel="Weekly Avg Flow [cfs]",
            yscale='log', xlim=[datetime.date(2003, 10, 1), datetime.date(2003, 10, 30)])
    ax.legend()
    plt.show()

    fig.set_size_inches(10,3)
    fig.savefig("Observed_Flow#6.png")