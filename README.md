# ScreenLock Pro
Easy open-source screen locker for Windows. Created with .NET C# Winforms.

# Requirements
 - Installed .NET 6
 - Windows OS (10+)
 
# Features
 - Killing explorer (blocking WIN key)
 - Disabling master volume
 - Restoring previous state before locking, when unlocking
 - Add itself to startup (using task scheduler, it's faster)
 - Two factor verification on bad attempts (optional)
 - PBKDF2-HMAC-SHA256 password hashing
 
# More
This program doesn't encrypt your files, it'll just lock your screen from being accessed/viewed.

# Possible bugs
 - Program may not be scaled correctly
 - Volume level may not be restored automatically, if you restart PC

# Removal
1. Press CTRL+ALT+DEL (when not on timeout)
   - Restart PC by clicking Power button and holding SHIFT, when pressing Restart
   - Troubleshooting screen should appear, if not, you're doing something wrong
2. Troubleshoot -> Advanced options -> Startup Settings => Press Restart
   - After restarting, you'll see a menu.
     - Press F4, or just 4

3. When you boot, you'll probably see your desktop is different and screen locker didn't start
   - Press WIN+R -> enter "taskschd.msc /s" without quotes => press enter OR press WIN and open app "Task Scheduler"
   - In task scheduler, open a root folder and find task "screenlockpro_startup" => delete this task, don't disable
   - If you deleted, restart your PC normally, do NOT go again to troubleshoot menu
4. When you login after restarting PC, screen locker should not start
   - Screen locker probably have some stored files and they will not be deleted automatically by windows, cause it's not saved in temp folder.
     - To remove temporary files created by screen lock, start screen locker app again, you'll probably get a list of temporary files.
       - Press 'Delete', if you don't want to lock your PC again, after pressing Delete simply close main password-setup window.
