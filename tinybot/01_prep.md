# Step 1: Preparation

Complete these steps **before** the workshop.

## Important Notes

- **Mac users:** macOS Sonoma or later is required.
- **iPhone users:** iOS 17.3.1 or later is required.
- **Company-issued phones will not work.** Please bring a personal phone.

## 1. Install Visual Studio Code and Git

- [Download Visual Studio Code](https://code.visualstudio.com/)
- [Download Git](https://git-scm.com/download/win) (Windows users)

## 2. Clone the TinyBot Repository

Clone the TinyBot repo to your computer:

1. Open a terminal (or right-click on your desktop and select "Git Bash Here" on Windows).
2. Run:
   ```
   git clone https://github.com/imandel/tiltybot.git
   ```

## 3. Install PlatformIO in VS Code

1. Open VS Code.
2. Go to **View > Extensions** and search for **PlatformIO**.
3. Click **Install**.
4. Wait for initialization to complete (check the bottom-right corner of VS Code for progress).
5. Click **Reload Now** when prompted.

## 4. Build the Project

1. Open the cloned repo in PlatformIO: click the **ant icon** on the sidebar > **Quick Access** > **Open** > select the TinyBot repo folder.
2. In the file explorer, select `platformio.ini` to verify it opened correctly.
3. Click the **checkmark button** at the bottom of VS Code to build the project.

If the build succeeds, you're ready for the workshop!

---

**Next step:** [Software Setup](02_software.md)
