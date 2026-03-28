Flashy 🃏
A French–English vocabulary flashcard app built with Python and Tkinter. Cards auto-flip after 3 seconds to reveal the English translation. Words you already know get removed from the deck — so every session is focused on what you haven't learned yet.

How It Works

A random French word appears on the front of the card.
After 3 seconds, the card flips to show the English translation.
You decide:

✅ Right button — you knew it. Word is removed from your learning list.
❌ Wrong button — you didn't. Word stays in the deck for next time.


Progress is saved automatically to data/Words_to_learn.csv.


Project Structure
flashy/
│
├── data/
│   ├── french_words.csv       # Full word list (source data, don't delete)
│   └── Words_to_learn.csv     # Auto-generated: your remaining words
│
├── images/
│   ├── card_front.png
│   ├── card_back.png
│   ├── right.png
│   └── wrong.png
│
└── main.py

Data Format
french_words.csv and Words_to_learn.csv both follow this structure:
ColumnDescriptionFrenchThe French vocabulary wordEnglishIts English translation

Getting Started
Prerequisites

Python 3.x
pandas

bashpip install pandas
Run
bashpython main.py
On first run, the app reads from french_words.csv. Once you start marking words as known, it creates and reads from Words_to_learn.csv automatically.
To reset progress and start from scratch, delete Words_to_learn.csv.

Built With

tkinter — GUI
pandas — CSV read/write
random — card selection


What I Learned

Tkinter Canvas and image rendering
Tkinter after() for timed events and cancellation with after_cancel()
Persistent state with pandas DataFrames and CSV
Handling FileNotFoundError for first-run logic
