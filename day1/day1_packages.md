---

````markdown
# 🧩 Day 1 – Linux Package Management (APT & dpkg)

**Date:** November 1, 2025  
**Author:** Elad Amar (@elad46)  
**Project:** LPIC-1 Practice & DevOps Journey  
**System:** Ubuntu 24.04.3 LTS (WSL2)

---

## 🎯 Learning Objectives
- Understand how Linux manages and installs software packages  
- Learn to use the **APT** (Advanced Package Tool) command line  
- Practice installing, updating, and removing packages safely  
- Understand dependencies and system updates  

---

## 📦 Commands Practiced

| Command | Description |
|----------|--------------|
| `sudo apt update` | Refreshes the local package list |
| `sudo apt upgrade` | Updates all installed packages to the newest version |
| `sudo apt install htop -y` | Installs the package `htop` automatically |
| `apt search <name>` | Searches for a package in repositories |
| `apt policy <name>` | Shows from which source a package will be installed |
| `sudo apt remove <name>` | Removes the package but keeps configuration files |
| `sudo apt purge <name>` | Removes package + configuration files |
| `sudo apt autoremove -y` | Removes unneeded dependency packages |
| `sudo apt clean` | Cleans cached package files |
| `uname -a` | Displays kernel and system information |

---

## 🧠 Key Concepts Learned

- **Package:** a software component with all files needed to install a program.  
- **Repository:** a collection of verified packages the system downloads from.  
- **Dependency:** supporting libraries or packages needed for another program to run.  
- **APT vs dpkg:**  
  - `apt` installs from repositories.  
  - `dpkg` installs from local `.deb` files.  
- **sudo:** executes commands with administrative (root) privileges.  

---

## 💻 Practical Exercise

```bash
# Update local package lists
sudo apt update

# Install htop
sudo apt install htop -y

# Run htop
htop

# Exit htop (press 'q')
# Remove htop
sudo apt remove htop -y
sudo apt purge htop -y

# Clean system
sudo apt autoremove -y
sudo apt clean

# Check system info
uname -a
````

---

## 🪄 Output Example

```bash
Distributor ID: Ubuntu
Description:    Ubuntu 24.04.3 LTS
Release:        24.04
Codename:       noble
Linux elad 6.6.87.2-microsoft-standard-WSL2 x86_64 GNU/Linux
```

---

## 📚 Notes

* Linux handles all installations via repositories — no manual downloading needed.
* Using the terminal is faster and more reliable than a GUI installer.
* You can track all installed packages with `dpkg -l`.

---

## ✅ Summary

Today I successfully:

* Installed and removed software packages using APT.
* Learned about dependencies and repositories.
* Cleaned and verified system integrity.

> 🧠 *"Real admins don’t double-click installers – they type apt install."*

---

## 🔗 Next Steps

* Day 2: Learn about `/etc/apt/sources.list` and Snap package management.
* Add a Python exercise (`day1_functions.py`) to this folder.
* Commit & push all files to GitHub repository:

  ```
  linux-lpic1-practice
  ```

---

```

---

💡 ככה בדיוק זה ייראה בגיטהב — מסודר, צבעוני, מקצועי וקריא.  
אפשר גם להוסיף בהמשך צילום מסך קטן מ־`htop` או הפלט שלך עם `uname -a`.  

רוצה שאכין לך עכשיו גם את **README הראשי של כל הריפו** (עם כותרת, רשימת ימים ואייקונים)?  
זה ישב בקובץ `README.md` וייתן לריפו שלך מראה של פרויקט אמיתי ללימוד LPIC-1.
```
