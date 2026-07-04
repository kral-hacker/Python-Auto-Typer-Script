# Auto Typing Script

A simple Python automation script that uses `pyautogui` to automatically type a predefined block of text after a short delay.

## Features

- Waits for a specified amount of time before starting.
- Automatically types the provided text.
- Adjustable typing speed.
- Useful for demonstrations, testing, or repetitive typing tasks.

## Requirements

- Python 3.x
- pyautogui

Install the required package:

```bash
pip install pyautogui
```

## How to Use

1. Replace the contents of the `text` variable with the text you want to type.
2. Save the script.
3. Run the script:

```bash
python main.py
```

4. Immediately click on the application (Notepad, Word, browser, chat window, etc.) where you want the text to be typed.
5. The script waits **7 seconds** to give you time to switch to the target window.
6. After the delay, it begins typing automatically.

## Configuration

### Change the Delay

Modify the delay before typing starts:

```python
time.sleep(7)
```

Example: Wait 10 seconds.

```python
time.sleep(10)
```

### Change the Typing Speed

Modify the interval between keystrokes:

```python
pt.write(text, interval=0.01)
```

Examples:

- Faster:

```python
interval=0.005
```

- Slower:

```python
interval=0.05
```

## Example

```python
text = """
Hello!
This text was typed automatically using Python.
Have a great day!
"""
```

## Warning

- Once the timer expires, the script will type wherever your cursor is focused.
- Make sure the correct application or text field is selected before the countdown ends.
- Avoid moving the focus to sensitive applications while the script is running.
