# TYPING-SPEED-TESTER
This project is a **Typing Speed Test application written in x86 Assembly** using the Irvine32 library.  
It allows users to test their typing speed and accuracy in real time and stores previous results.

---

## 📌 Features

✅ Menu-driven interface  
✅ Measures:
- Elapsed time (ms)
- Correct characters
- Mistakes
- Accuracy (%)
- Words Per Minute (WPM)

✅ Converts input to uppercase for fair comparison  
✅ Compares input with a reference sentence  
✅ Stores up to 10 previous WPM results (circular stack)  
✅ Displays stored results  

---

## 🧠 How It Works

The program performs the following:

1. Displays a menu:
   - Start Typing Test
   - Show Previous Results
   - Exit

2. When testing:
   - Shows a reference sentence  
   - Starts timer using `GetTickCount`
   - Reads user input
   - Converts both input and sentence to uppercase
   - Compares characters one by one
   - Counts:
     - Correct characters
     - Mistakes

3. Calculates:
Accuracy % = (correct * 100) / sentence length
WPM = (correct * 12000) / elapsed_ms


4. Stores WPM in a **circular stack of size 10**

---

## 🛠️ Technologies Used

- x86 Assembly Language
- Irvine32 Library
- MASM32
- Windows Console

---

## 📂 Program Components

### Main Features in Code

- Menu System
- Input Handling
- Timer with `GetTickCount`
- String Conversion (uppercase)
- Character Comparison
- Math Calculations
- Circular Result Storage
- Console Output

---

## ▶️ How to Run

✅ Requirements:

- MASM / TASM environment
- Irvine32 library installed
- Windows OS

### Build & Run (MASM)

ml /c /coff main.asm
link /subsystem:console main.obj Irvine32.lib
main.exe


---

## 📊 Example Output

---- TYPING SPEED TESTER ----

Start Typing Test

See Previous Results

Exit
Enter choice: 1

Type the sentence and press ENTER:
THE QUICK BROWN FOX JUMPS OVER THE LAZY DOG


After typing:

Results:
Elapsed (ms): 2450
Correct chars: 41
Mistakes: 3
Accuracy (%): 93
WPM: 200


---

## 🚧 Future Improvements

- Support multiple test sentences
- Better WPM calculation (word-based)
- GUI version
- High score saving to file
- Backspace handling

---

## 📜 License

This project is open-source and free to use.
