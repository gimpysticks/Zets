https://live.warthunder.com/dl/ff7dda4b56d4349f03bcb55a2e4dddba77ba1976/
I can't paste urls into war thunder on steam for linux

import pyautogui
import time

def send_clipboard_as_keystrokes():
    # Get the current clipboard content
    clipboard_content = pyautogui.paste()

    # Simulate key presses to type out the clipboard content
    pyautogui.typewrite(clipboard_content)

    # Wait for a short moment before ending the script
    time.sleep(1)

send_clipboard_as_keystrokes()

