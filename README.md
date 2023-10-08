import pandas as pd
import matplotlib.pyplot as plt

file_path = '/kaggle/input/bundesliga-soccer-player/bundesliga_player.csv'

df = pd.read_csv(file_path)

top_10_players = df.nlargest(10, 'market_value')

plt.bar(top_10_players['player_name'], top_10_players['market_value'])

plt.xlabel('Player')
plt.ylabel('Market Value')

plt.title('Top 10 Players with Highest Market Value')

plt.xticks(rotation=90)

plt.show()
