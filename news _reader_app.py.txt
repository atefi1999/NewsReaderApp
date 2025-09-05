class News:
    def __init__(self, title, content, category, author, date):
        self.title = title
        self.content = content
        self.category = category
        self.author = author
        self.date = date

    def __str__(self):
        return f"Title: {self.title}\nContent: {self.content}\nCategory: {self.category}\nAuthor: {self.author}\nDate: {self.date}"


class NewsManager:
    def __init__(self):
        self.news_list = []  # List to store news

    def add_news(self, news):
        """Add a news item to the list"""
        self.news_list.append(news)

    def remove_news(self, news):
        """Remove a news item from the list"""
        if news in self.news_list:
            self.news_list.remove(news)

    def list_news(self):
        """Display all news"""
        for i, news in enumerate(self.news_list, start=1):
            print(f"\n--- News {i} ---")
            print(news)

    def find_news_by_title(self, title):
        """Search for news by title"""
        for news in self.news_list:
            if news.title == title:
                return news
        return None

    def list_by_category(self, category):
        """Display all news by a specific category"""
        filtered_news = [news for news in self.news_list if news.category == category]
        for i, news in enumerate(filtered_news, start=1):
            print(f"\n--- News {i} ---")
            print(news)


class User:
    def __init__(self, username, email):
        self.username = username
        self.email = email
        self.saved_news = []  # List of saved news

    def save_news(self, news):
        """Save a news item in saved_news"""
        if news not in self.saved_news:
            self.saved_news.append(news)
            print(f"✅ News '{news.title}' saved for user {self.username}.")
        else:
            print(f"ℹ️ News '{news.title}' is already saved.")

    def list_saved_news(self):
        """Display the user's saved news"""
        if not self.saved_news:
            print("❌ You haven't saved any news yet.")
        else:
            print(f"\n📌 Saved news by {self.username}:")
            for i, news in enumerate(self.saved_news, start=1):
                print(f"\n--- News {i} ---")
                print(news)


# ---------------- Sample Run ----------------
if __name__ == "__main__":
    # Create a news manager
    manager = NewsManager()

    # Create some sample news
    news1 = News("First News", "This is the first news content.", "Politics", "Ali Rezaei", "2025-09-04")
    news2 = News("Second News", "This is the second news content.", "Sports", "Maryam Ahmadi", "2025-09-03")
    news3 = News("Third News", "This is the third news content.", "Politics", "Hossein Mohammadi", "2025-09-02")

    # Add news items
    manager.add_news(news1)
    manager.add_news(news2)
    manager.add_news(news3)

    # Display all news
    manager.list_news()

    # Display news by category
    print("\n📌 Political News:")
    manager.list_by_category("Politics")

    # Search by title
    found = manager.find_news_by_title("Second News")
    if found:
        print("\n✅ News found:")
        print(found)

    # Create a user
    user = User("reza", "reza@example.com")

    # Save news for the user
    user.save_news(news1)
    user.save_news(news2)
    user.save_news(news1)  # Test duplicate save

    # Display saved news for the user
    user.list_saved_news()


