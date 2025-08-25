# Ex.No: 01A PLOT A TIME SERIES DATA


# AIM:
To Develop a python program to Plot a time series data (population/ market price of a commodity
/temperature.
# ALGORITHM:
1. Import the required packages like pandas and matplot
2. Read the dataset using the pandas
3. Calculate the mean for the respective column.
4. Plot the data according to need and can be altered monthly, or yearly.
5. Display the graph.
# PROGRAM:


            import pandas as pd
            import matplotlib.pyplot as plt
            
            # Load the CSV file correctly
            data = pd.read_csv(r'C:\Users\admin\Downloads\favorite_music_dataset.csv')
            
            # Convert 'Listened_Date' to datetime
            data['Listened_Date'] = pd.to_datetime(data['Listened_Date'])
            
            # Count number of songs listened per day
            daily_counts = data.groupby('Listened_Date').size()
            
            # Plot time series for daily songs listened
            plt.figure(figsize=(10, 6))
            plt.plot(daily_counts.index, daily_counts.values, label='Songs Listened per Day', color='purple')
            
            plt.title('Daily Songs Listened Over Time')
            plt.xlabel('Date')
            plt.ylabel('Number of Songs')
            plt.grid(True)
            plt.legend()
            
            plt.show()









# OUTPUT:



<img width="1241" height="681" alt="Screenshot 2025-08-25 151918" src="https://github.com/user-attachments/assets/efa64466-faf5-4fd3-99d2-ea7650754341" />





# RESULT:
Thus we have created the python code for plotting the time series of given data.
