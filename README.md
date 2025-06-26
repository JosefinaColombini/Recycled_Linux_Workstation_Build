# 🧰 Recycled Linux Workstation

## 🔐 Why This Project?

This project is my personal starting point to dive deeper into the world of cybersecurity and hands-on tech.

I built this machine not just to reuse old parts, but to gain real experience assembling a PC from scratch — understanding how hardware works, what components are compatible, and how everything fits together.

With Parrot OS installed, my goal is to improve my Linux skills, start learning about offensive security (like penetration testing), and explore how SOC (Security Operations Center) teams monitor and respond to threats.

In the future, I plan to expand this lab by adding network devices like switches and routers to gain hands-on experience with networking, traffic analysis, and more advanced security monitoring.

This recycled PC is my gateway to learning by doing — no fancy hardware required.

---

## 🧱 Hardware Specs

| Component         | Details                                |
|------------------|----------------------------------------|
| **Case**         | Generic mid-tower from an old PC       |
| **Motherboard**  | H81H3-M4 (LGA 1150, DDR3 support)       |
| **CPU**          | Intel Core i3-4170 (2 cores, 3.7GHz)    |
| **RAM**          | 6GB DDR3 1333MHz                        |
| **Storage**      | 1TB Seagate HDD                         |

---

## 🐧 Operating System

- **Distro**: [Parrot OS Home Edition](https://www.parrotsec.org/)
- **Purpose**: Learning fundamentals, Linux experimentation, Security research

---

## 🎯 Project Goals

- ✅ Build a working PC from recycled parts  
- ✅ Install and configure Parrot OS  
- ⏳ Set up a home cybersecurity lab  
- ⏳ Practice Linux CLI and bash scripting  
- ⏳ Explore SOC tools, log analysis, and monitoring  

---
## 🛠 Troubleshooting Process

While building and setting up this recycled Linux workstation, I encountered several issues. Here’s how I identified and solved each one, showcasing some of my basic troubleshooting workflow:

### 1. 🖥️ Computer Wouldn’t Boot

- **Initial Assumption:** I thought the power cable might be connected incorrectly on the motherboard.
- **What I Did:** I carefully re-read the motherboard's manufacturer manual multiple times, and the power connections appeared correct.
- **Next Step:** I suspected the Power Supply Unit (PSU) might be faulty.
- **Test Performed:** I used the paperclip trick (a basic PSU test) to see if the PSU fan would spin. It didn’t.
- **Solution:** I found a PSU from an old computer, connected it, and the system powered on successfully. This confirmed the original PSU was dead.

### 2. 🧪 Linux Installation Boot Issue

- **Distro Chosen:** Parrot OS Home Edition – selected because it's lightweight and suited for systems with limited resources.
- **Flashing Tool Used:** Balena Etcher – as recommended in Parrot OS documentation.
- **Problem Encountered:** When trying to boot from the USB, I received a “Security Violation” error.
- **Diagnosis:** After some research, I learned that this was caused by UEFI Secure Boot, which was preventing the unsigned OS from booting.
- **Fix:** I entered the BIOS/UEFI settings and changed the boot mode from **UEFI** to **Legacy**.
- **Result:** The system booted into the USB without issues and I was able to install Parrot OS successfully.


### 3. 🔌 No Operating System After Removing USB

- **Initial Assumption:** The computer likely didn't install the OS to the internal hard drive and was running in Live mode.
- **What I Did:**  Powered on the computer and tried running the Live mode again since it was the only option available.  
                   This appeared on the screen: ![IMG_3397](https://github.com/user-attachments/assets/1beeb33a-c50d-420e-9f13-2dc35a50548c)

- **Next Step:** Checked the hardware (faster than rebooting to troubleshoot software issues) and noticed the SATA power cable was poorly connected.
- **Fixing the Root Cause:** Turned off the system, reconnected everything correctly, rebooted to check if the BIOS recognized the HDD (all good), and proceeded with installing ParrotOS.
- **Finishing up:** The only last thing left was to properly install ParrotOS and I chose the SwapFile option because I recently learnt about Virtual Memory and was excited about it, also i know 6Gb aren't the greatest thing (fyi: i chose swapfile because it's easier to resize or remove if needed).
- **Additional Notes:**  I also saw that the documentation recommended 4GB of RAM (though documentation says it works with less), so I added an extra DDR3 RAM stick. It’s 1333Hz, so my system now runs 6GB of RAM at 1333Hz, even though one of the sticks is 1600Hz. Since I’m not doing heavy multitasking, it should work fine.


---

## 📸 Hardware Screenshots
I know the components don’t exactly match the PC case — it's a bit of a mismatch — but I managed to make everything fit and function properly, while making sure the PSU still had enough ventilation.

![IMG_3383](https://github.com/user-attachments/assets/cbb1e6b2-3450-4d7e-97d7-e2660eebe96c)

This is the best (free) RAM i could find - sadly:
![IMG_3382](https://github.com/user-attachments/assets/7e49d9d9-8d95-42f0-8c2e-325efb8f8363)

Lastly, i had two options for the HDD and decided to go for 1tb (the seagate one) because i don't trust the PS to be strong enough:
![IMG_3377](https://github.com/user-attachments/assets/bb30fd4f-f547-4681-95d5-15482a1d7e0a)

## 📸 Software Screenshots
Here’s a screenshot of the BIOS main screen, showing the settings I had to adjust for reference:

![IMG_3395](https://github.com/user-attachments/assets/606cd7c1-dfe8-47f7-8ed4-66fe5db73389)
![IMG_3396](https://github.com/user-attachments/assets/5cc369ed-2f36-47a0-8b29-35ed6cfde360)

---


