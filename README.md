toggle := false

F1::
toggle := !toggle
While toggle
{
    Click
    Sleep, 100 ; Adjust the speed (in milliseconds) as needed
}
return

F2::ExitApp ; Press F2 to exit the script
import pyautogui
import time
import keyboard

print("Hold down 'F1' to click. Press 'F2' to exit.")
try:
    while True:
        if keyboard.is_pressed('F1'):  # While F1 is held down
            pyautogui.click()
            time.sleep(0.1)  # Adjust the speed (in seconds) as needed
        elif keyboard.is_pressed('F2'):  # Press F2 to exit
            print("Stopped.")
            break
except KeyboardInterrupt:
    print("Stopped.")
