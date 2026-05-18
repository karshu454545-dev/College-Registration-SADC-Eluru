# 📋 Student Enquiry Form — WhatsApp Integration

A smart student enquiry form that instantly sends registration details directly to a WhatsApp number — built with HTML, CSS, and JavaScript.

![HTML](https://img.shields.io/badge/HTML-E34F26?style=flat&logo=html5&logoColor=white)
![CSS](https://img.shields.io/badge/CSS-1572B6?style=flat&logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat&logo=javascript&logoColor=black)
![WhatsApp](https://img.shields.io/badge/WhatsApp_API-25D366?style=flat&logo=whatsapp&logoColor=white)

## 🔗 Live Demo
👉 [Click here to view the form](https://karshu454545-dev.github.io/College-Registration-SADC-Eluru/)

## 📸 About the Project
This is a real-world student enquiry form built for **SADC Eluru College**. When a prospective student fills in their details and clicks Submit, the form automatically opens WhatsApp with a pre-filled, neatly formatted message sent directly to the college's WhatsApp number — no backend or server needed!

## ✨ Features
- 👤 Student name input
- 📞 Mobile number input
- 🎓 Course selection via dropdown (all college courses listed)
- 💬 On submit, auto-opens WhatsApp with a formatted message
- 📲 Works on both mobile and desktop
- ⚡ No backend required — fully frontend powered
- 📱 Mobile-friendly with responsive viewport

## 📩 WhatsApp Message Format
When the form is submitted, the following message is automatically sent to the college WhatsApp number:

```
New Student Registration

Name: Karishma
Mobile: 1873828392
Course: BSc Computers
```

## 🛠️ Technologies Used
| Technology | Purpose |
|---|---|
| HTML5 | Form structure, input fields, dropdown |
| CSS3 | Styling and layout |
| JavaScript (ES6) | Form data collection, message formatting, WhatsApp URL generation |
| WhatsApp API (`wa.me`) | Sending pre-filled messages to a WhatsApp number |

## 🧠 How It Works
1. Student fills in their **Name**, **Mobile Number**, and selects a **Course**
2. On clicking **Submit**, JavaScript collects all the form values
3. A formatted message string is built using **template literals**
4. The message is encoded using `encodeURIComponent()` to make it URL-safe
5. The browser opens `https://wa.me/NUMBER?text=MESSAGE` — launching WhatsApp with the pre-filled message
6. The college receives the enquiry instantly on WhatsApp — no server needed!

## 💻 Core JavaScript Logic
```javascript
const name = document.getElementById("name").value;
const mobile = document.getElementById("mobile").value;
const course = document.getElementById("course").value;

const message = `New Student Registration\n\nName: ${name}\nMobile: ${mobile}\nCourse: ${course}`;

const url = `https://wa.me/YOURNUMBER?text=${encodeURIComponent(message)}`;
window.open(url);
```

## 🚀 How to Run Locally
1. Clone the repository:
   ```bash
   git clone https://github.com/karshu454545-dev/College-Registration-SADC-Eluru.git
   ```
2. Open `index.html` in your browser.
3. Fill in the form and click Submit — WhatsApp will open automatically!

## 🎯 What I Learned
- Using the **WhatsApp `wa.me` API** to send pre-filled messages from a browser
- Building and formatting dynamic strings using **JavaScript template literals**
- Encoding special characters for URLs using `encodeURIComponent()`
- Collecting and validating form data using JavaScript
- Building a **real-world, practical tool** with zero backend

## 👩‍💻 Author
**Karishma Shaik**
- GitHub: [@karshu454545-dev](https://github.com/karshu454545-dev)
- LinkedIn: [Karishma Shaik](https://www.linkedin.com/in/karishma-shaik-g2707)
