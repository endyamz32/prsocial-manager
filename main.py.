
import csv
from collections import Counter

INPUT_FILE = "targets.csv"

def main():
    accounts = set()

    with open(INPUT_FILE, encoding="utf-8") as file:
        reader = csv.DictReader(file)

        for row in reader:
            platform = row["platform"].strip().lower()
            username = row["username"].strip().lstrip("@")

            if platform in ("instagram", "tiktok") and username:
                accounts.add((platform, username))

    print("=== PR.SOCIAL TASK MANAGER ===")
    print("Total akun:", len(accounts))

    counts = Counter(p for p, u in accounts)

    print("Instagram:", counts["instagram"])
    print("TikTok:", counts["tiktok"])

    for platform, username in sorted(accounts):
        print(f"{platform}: @{username}")

if __name__ == "__main__":
    main()
    
