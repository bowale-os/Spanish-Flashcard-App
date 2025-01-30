### Spanish-Flashcard-App
A flashcard app that helps user learn basic Spanish words, created with the Tkinter GUI

This is a Python program using Tkinter to create a flashcard-style language learning app. Here's a breakdown of how it works:

### **Functionality**
- The app displays Spanish words with their English translations after 3 seconds.
- The user can mark words as known or unknown.
- Known words are removed from the learning list and saved in a separate CSV file (`words_to_learn.csv`).
- The app cycles through words randomly, allowing for spaced repetition learning.

---

### **Key Components**
1. **Data Handling**
   - The words are loaded from `spanish_words.csv` initially.
   - If `words_to_learn.csv` exists, it loads from there instead.
   - Words the user knows are removed from the list and saved to `words_to_learn.csv`.

2. **Flashcard Mechanism**
   - A random word is selected using `random.choice(df)`.
   - The front side displays the Spanish word.
   - After 3 seconds, the flashcard flips to reveal the English translation.
   - The user can either:
     - Press the ❌ button to move to the next word without saving.
     - Press the ✅ button to mark the word as known and remove it from the list.

3. **Tkinter GUI Elements**
   - A `Canvas` to display the flashcard.
   - Buttons (`right_btn`, `wrong_btn`) to interact with the app.
   - Images for visual appeal (`card_front.png`, `card_back.png`).
   - `window.after()` for the 3-second delay before flipping the card.

---

### **Potential Improvements**
- **Error Handling:** If `spanish_words.csv` is missing, the app should notify the user.
- **Progress Tracking:** Display progress (e.g., number of words left to learn).
- **Multiple Language Support:** Extend it to work with other language datasets.
- **Animations:** Smooth transitions when flipping the card.

