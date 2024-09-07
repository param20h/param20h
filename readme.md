import requests
from bs4 import BeautifulSoup

def fetch_gfg_stats(username):
    url = f"https://auth.geeksforgeeks.org/user/{username}/practice/"
    response = requests.get(url)
    soup = BeautifulSoup(response.text, 'html.parser')

    stats = {}
    stats['username'] = username
    stats['total_problems_solved'] = soup.find("div", class_="score_card_value").text.strip()
    # You can extend this to fetch more stats if needed

    return stats

def update_readme(stats):
    with open("README.md", "r") as file:
        lines = file.readlines()

    # Modify the lines to include your stats (implement your custom logic here)

    with open("README.md", "w") as file:
        file.writelines(lines)

if __name__ == "__main__":
    username = "param_06_"  # Replace with your GFG username
    stats = fetch_gfg_stats(username)
    update_readme(stats)
