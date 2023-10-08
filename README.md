import matplotlib.pyplot as plt

y_values = [0, 100, 200, 300, 400, 500, 600,]  # Added an additional value of 600
x_labels = ['to','a', 'your', 'call', 'or', 'the', '2', 'for', 'you', 'is', 'call', 'on', 'have', 'and', 'from', 'ur', 'with', '&', '4', 'of']
x_values = [600,370, 190, 190, 190, 180, 175, 175, 170, 160, 150, 150, 145, 140, 135, 130, 125, 120, 100, 100]

# Adjusting the figure size and dpi for better visual appearance
plt.figure(figsize=(10, 6), dpi=80)

# Creating an array of indices for x-axis positioning
x_indices = range(len(x_labels))

# Plotting the bars with adjusted width and color
plt.bar(x_indices, x_values, width=0.6, color='skyblue', edgecolor='black'

# Customizing the x-axis labels with rotation and font size
plt.xticks(x_indices, x_labels, rotation=45, fontsize=10, ha='right')

# Customizing the y-axis limits
plt.ylim(0, 600)  # Adjusted the y-axis limit to accommodate the additional value

# Customizing the y-axis label
plt.ylabel('Number')

# Customizing the chart title, font size, and weight
plt.title('More frequency words in spam messages', fontsize=12, fontweight='bold')

# Adding labels to the bars
for i, v in enumerate(x_values):
    plt.text(i, v + 20, str(v), color='black', ha='center', fontsize=8)

# Adding gridlines for better readability
plt.grid(axis='y', linestyle='--')

# Removing the top and right spines
plt.gca().spines['top'].set_visible(False)
plt.gca().spines['right'].set_visible(False)

# Adjusting the layout for better spacing
plt.tight_layout()

# Displaying the chart
plt.show()
