# How to connect to your desired VPN server (AmneziaVPN Client)

This guide explains how you can properly save your progress when playing Flash games locally (.swf files) using the standalone Adobe Flash Player.

---

## 🖱️ Step 1: Open the Flash Game

- Double-click your `.swf` file to open it with **Adobe Flash Player Projector**.
- Wait until the game has loaded.

---

## 🛠️ Step 2: Enable Local Storage

- **Right-click** anywhere inside the running Flash game window.
- Select **"Settings"** from the right-click menu.
- In the Settings popup:
  - Click the **folder icon** (this represents *Local Storage* settings).
  - Choose **"Allow"** to permit the game to store information on your computer.
  - Click **Close** once done.
    
![image](https://github.com/user-attachments/assets/0bcce3d5-494e-4b6a-8505-ea2cbdceff38)

This step is important! Without allowing local storage, your game progress might not be saved after closing.

---

## 💾 Step 3: Save the Game Inside the Game

- Use the **in-game save feature** (usually found in the game’s menu like *Save Game*).
- **Do not** immediately close the Flash Player after saving.  
  Let the save file be properly written.

---

## 📂 Step 4: Locate Your Save Files

Flash games save your progress as `.sol` files inside your computer.  
Here’s how you can find them:

1. Open **File Explorer** (`Win + E`).
2. Navigate to the following path:
   C:\Users\<YourUsername>\AppData\Roaming\Macromedia\Flash Player\#SharedObjects\
- Replace `<YourUsername>` with your Windows username.
  
  ![image](https://github.com/user-attachments/assets/ce965fe6-6607-48b6-8cac-d0cb567200ff)

3. Inside `#SharedObjects`, you will find one or more random-named folders.
4. Keep opening the folders until you find another sub-folder related to your Flash game (the folder name may match the game's website, or the game name).
5. Inside it, you will find `.sol` files — these are your **saved games**!
   
   ![image](https://github.com/user-attachments/assets/a1ace1f0-1f18-41da-a17b-94394b5f91ae)

  

---

## 📌 Important Notes

- If you plan to **move your game** to another computer, make sure to copy the `.sol` files as well.
- Some games create multiple `.sol` files for different save slots.
- If you clear Flash Player data or use certain cleaners, these save files may get deleted. Always backup if important!
- Highly recommended not to use the online-save feature in most games (They will bug out on your local Flash Player)

---

## 📣 Need Help?

Feel free to open an Issue on https://github.com/RoobusBoi/redhatvpnservices/issues if you encounter any problems!

---

