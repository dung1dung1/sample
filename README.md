plt.bar(top_10_players['name'], top_10_players['market_value'], color='green')

# Đặt tên cho trục x và trục y
plt.xlabel('Player')
plt.ylabel('Market Value')

# Đặt tiêu đề cho biểu đồ
plt.title('Top 10 Players with Highest Market Value')

# Xoay tên các cầu thủ để tránh chồng chéo
plt.xticks(rotation=45)

# Hiển thị biểu đồ
plt.show()
