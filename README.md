import pandas as pd
import matplotlib.pyplot as plt

# Đường dẫn đến tệp CSV
file_path = '/kaggle/input/bundesliga-soccer-player/bundesliga_player.csv'

# Đọc dữ liệu từ tệp CSV vào DataFrame
df = pd.read_csv(file_path)

# Sắp xếp theo giá trị thị trường giảm dần và lấy 10 hàng đầu
top_10_players = df.nlargest(10, 'market_value')

# Tạo biểu đồ cột
plt.bar(top_10_players['player_name'], top_10_players['market_value'])

# Đặt tên cho trục x và trục y
plt.xlabel('Player')
plt.ylabel('Market Value')

# Đặt tiêu đề cho biểu đồ
plt.title('Top 10 Players with Highest Market Value')

# Xoay tên của các cầu thủ để tránh việc chồng chéo
plt.xticks(rotation=90)

# Hiển thị biểu đồ cột
plt.show()
