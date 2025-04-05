# 🤖 WhatsApp Bot Using Only Selenium

A human-like WhatsApp messaging bot built with Python and Selenium to send personalized messages to customers through WhatsApp Web.

> ⚠️ **Disclaimer**: This tool is intended strictly for educational and personal use. Do **not** use it for spam or unsolicited messaging. Always comply with WhatsApp’s [terms of service](https://www.whatsapp.com/legal/terms-of-service).

---

## 🚀 Features

- Send personalized messages via WhatsApp Web
- Reads contact and message data from an Excel file
- Simulates human-like behavior (delays, retries)
- Batching system for message control
- Delivery log saved to Excel
- Error handling and retry mechanism

---

## 🧰 Tech Stack

| Technology | Version (Recommended) |
|------------|-----------------------|
| Python     | 3.8+                  |
| Selenium   | 4.10+                 |
| Pandas     | 1.5+                  |
| Chrome     | Latest Stable         |
| ChromeDriver | Compatible with your Chrome version |

---

## 📂 Folder Structure

```
📁 WhatsAppBot/
│
├── contacts.xlsx              # Excel file with customer names and phone numbers
├── Whatsapp_Bot_Using_Only_Selenium_final.ipynb
├── delivery_log.xlsx          # Auto-generated log after sending messages
├── README.md                  # Project documentation (this file)
```

---

## 📄 Input File Format

Create a file called `contacts.xlsx` with the following columns:

| Business Name | Phone Number     |
|---------------|------------------|
| John Traders  | +919812345678    |
| XYZ Co.       | +919812345678    |

- Phone numbers are automatically formatted to international format.
- Messages are personalized like:
  ```
  Hello John Traders, thank you for your support! - Regards Apex Strategies Inc.
  ```

---

## 🧠 Approach

1. **Data Preparation**  
   - Reads and validates contacts from an Excel sheet.
   - Auto-formats numbers and creates messages.

2. **WhatsApp Authentication**  
   - Launches Chrome and navigates to WhatsApp Web.
   - Waits for the user to scan the QR code manually.

3. **Message Delivery**  
   - Navigates to individual chat URLs using phone numbers.
   - Waits for input field, types message, and hits Enter.
   - Batches are sent with optional delay and retry handling.

4. **Logging**  
   - All message attempts (sent/failed) are saved to `delivery_log.xlsx`.

---

## 🛠️ Setup & Installation

### 1. Clone the Repo

```bash
git clone https://github.com/Bhole-Nath/whatsapp-bot-selenium.git
cd whatsapp-bot-selenium
```

### 2. Install Dependencies

Make sure you have Python installed, then install required libraries:

```bash
pip install selenium pandas openpyxl
```

> ⚠️ Also, ensure **ChromeDriver** is installed and matches your Chrome version:
- [Download ChromeDriver](https://sites.google.com/a/chromium.org/chromedriver/downloads)
- Place it in your system `PATH` or modify the script to include the full path.

### 3. Add Your Contacts

Create a `contacts.xlsx` as shown above.

---

## 🧪 Run the Bot

### Option 1: Run as Python Script

```bash
python Whatsapp_Bot_Using_Only_Selenium_final.ipynb
```

(Or convert it to `.py` and run normally.)

### Option 2: Open in Jupyter Notebook

```bash
jupyter notebook Whatsapp_Bot_Using_Only_Selenium_final.ipynb
```

---

## ✅ Best Practices

- Always send messages in **small batches**
- Never message users without **their explicit consent**
- Use a **dedicated WhatsApp account** for testing
- Check message **delivery logs** to track failures

---

## 📈 Roadmap / Ideas

- [ ] Integrate with a database
- [ ] Add message templating system
- [ ] Automate QR scan using session storage
- [ ] Add multilingual support

---

## 🧑‍💻 Author

**Nikhil Chavhan (Alias: Bhole-Nath)**  
_A project by Apex Strategies_  
🌐 [Website](https://apexstrategies.com)

---

## 📜 License

This project is open-source and free to use under the [MIT License](LICENSE).

---

## 🙏 Acknowledgements

- Selenium WebDriver Team
- Pandas Devs
- The Open Source Community ❤️
