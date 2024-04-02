# Setting Up a Raspberry Pi Headless (SSH) Connection
By: Connor Robinson, Aidan Costello, Thomas Elpers, Abel Lu

By following these steps, you’ll be able to connect to your Raspberry Pi
headless using SSH and Nmap. 🎩🍓

## 1. Get the Raspberry Pi Imager
- Visit the official Raspberry Pi website or the GitHub repository to download the
  Raspberry Pi Imager tool.
- Choose the version suitable for your operating system (Windows, macOS, or Linux).
## 2. Download the Correct OS for the Pi
- Launch the Raspberry Pi Imager tool.
- Select the appropriate operating system for your Raspberry Pi.
  For headless setup (without a graphical user interface), consider using Raspberry Pi OS Lite.
- Follow the prompts to download and write the OS image to your microSD card.
## 3. Configure Settings in the Imager
- Before writing the OS image to the microSD card, configure Wi-Fi and enable SSH:
  - Click on “Choose OS” and select the OS image you’ve downloaded.
  - Click on “Choose SD Card” and select your microSD card.
  - Click on “Wireless Network” and enter your Wi-Fi credentials.
  - Enable SSH by clicking on “Interfacing Options” and checking the “SSH” option.
  - Click on “Write” to flash the OS image to the microSD card with the configured settings.
## 4. Download the CLI Version of Nmap
- Visit the official Nmap website and download the command-line version suitable
  for your operating system.
- Follow the installation instructions provided for your platform.
## 5. Open Your Computer’s CLI
On macOS:
- Open the Terminal application (you can find it in the Utilities folder within Applications).
  
On Windows:
- Open the Command Prompt (search for “cmd” in the Start menu).
## 6. Run the Correct Nmap Scan 
- Use Nmap to scan your local network for devices:

`nmap -sn 192.168.1.0/24`

- Replace 192.168.1.0/24 with your actual network range.

## 7. Decipher Which Open Port is Your Raspberry Pi
- Look for an open SSH port (default is port 22) associated with a device in the scan results.
  Note down the IP address of the Raspberry Pi.

## 8. SSH into Your Raspberry Pi
- On macOS:
  - Open the Terminal
  - Use SSH to connect to your Raspberry Pi:
    - `ssh pi@<RaspberryPi_IP>`
  - Replace `<RaspberryPi_IP>` with the IP address you noted down.
- On Windows:
  - You’ll need an SSH client like PuTTY.
  - Open PuTTY.
  - Enter the Raspberry Pi’s IP address and click “Open.”
  - Log in with the username (pi) and password (default is raspberry).
 
## 9. Make a New File
- Once connected via SSH, create a new file using a text editor like Nano or Vim:
  - `nano hello_world.txt`
- Write "Hello World" into the file.
- Save and exit the text editor.

## 10. Exit from Raspberry Pi
- To exit from the Raspberry Pi terminal, type:
  - `exit`

## 11. Test the Connection Again
- Repeat step 8 to SSH into your Raspberry Pi and ensure you can still connect successfully.




