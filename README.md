# 💍 Klinkatsis Wedding Website

A sophisticated Flask web application designed to celebrate and streamline the **Klinkatsis wedding**, featuring intuitive RSVP management, immersive travel pages, and custom-designed sections tailored for guests.  

Built with love and attention to detail, this project combines interactivity, style, and seamless navigation to make wedding planning both elegant and effortless.

---

## 🌟 Features

- 🗓️ **RSVP Form** — Guests can easily confirm or update their attendance, with responses stored securely in the local SQLite database (`wedding.db`). Real-time validation ensures accurate and up-to-date guest information.  

- 🏙️ **City Pages** — Travel pages for nearby cities are generated dynamically from a list of templates, making it easy to add new cities. Each page includes images, descriptions, and links for trip planning, styled consistently with cities.css.

- 💬 **Interactive Chatbot** — A friendly, keyword-based chatbot that recognizes logged-in guests and addresses them by name. It answers questions about the wedding, travel, and registry in real time. Its modular design allows for easy expansion with additional responses.

- 🔐 **Login System** — Simple name-based authentication with secure logout functionality, enabling personalized experiences for each guest and allowing the chatbot to tailor responses accordingly. 

- 💞 **Custom Design** — Multiple themed CSS files tailor the look and feel of different site sections (RSVP, login, chatbot, cities), creating a polished, cohesive, and user-friendly interface.  

- 📅 **Countdown Timer** — A dynamic countdown displays the remaining time until the wedding, providing an engaging, real-time element for guests to enjoy.

---

## ⚙️ Tech Stack

Backend:  
- Python 3  
- Flask (Jinja2 templating)  
- SQLite (wedding.db)  

Frontend:  
- HTML  
- CSS  
- JavaScript  

---

## 🗂️ Folder Structure

wedding-website/
│
├── README.md
├── .gitignore
├── app.py
├── guest_list.py
├── requirements.txt
├── instance/
│   └── wedding.db
│
├── static/
│   ├── css/
│   │   ├── chatbot.css
│   │   ├── checkstatus.css
│   │   ├── cities.css
│   │   ├── countdown.css
│   │   ├── login.css
│   │   ├── mr_mrs.css
│   │   ├── rsvp.css
│   │   └── styles.css
│   ├── js/
│   │   ├── chatbot.js
│   │   └── countdown.js
│   └── images/
│       ├── anaheim.jpg
│       ├── dana_point.jpg
│       ├── irvine.jpg
│       ├── laguna.jpg
│       ├── los_angeles.jpg
│       ├── newport_beach.jpg
│       ├── san_clemente.jpg
│       ├── san_diego.jpg
│       ├── marisabill.jpg
│       ├── Logo.jpg
│       └── wedding-bg.jpg
│
├── templates/
│   ├── base.html
│   ├── checkstatus.html
│   ├── main_pages/
│   │   ├── index.html
│   │   ├── login.html
│   │   ├── rsvp.html
│   │   ├── registry.html
│   │   ├── mr_mrs.html
│   │   ├── faq.html
│   │   └── travel.html
│   └── cities/
│       ├── anaheim.html
│       ├── dana_point.html
│       ├── irvine.html
│       ├── laguna.html
│       ├── los_angeles.html
│       ├── newport_beach.html
│       ├── san_clemente.html
│       └── san_diego.html
│   
│
└── weddingbot/
    ├── __init__.py
    ├── globals.py
    └── main.py


---

## 🚀 Getting Started

1. Set Up Your Environment

Create and activate a virtual environment (recommended):

python3 -m venv venv
source venv/bin/activate  # macOS / Linux
# or
venv\Scripts\activate     # Windows

2. Install Dependencies

pip install flask
pip install flask_sqlalchemy  # if using SQLAlchemy

3. Run the App

Make sure you’re in the project’s root folder (where app.py is), then run:

flask run
# or
python app.py

By default, it will run at:
http://127.0.0.1:5000

---

## 🧩 How It Works

### Templates & Routing
- Each HTML file under `templates/` corresponds to a route in `app.py` and extends `base.html` for consistent headers, footers, and navigation.  
- Flask uses Jinja2 templating to inject server-side dynamic content, including personalized greetings, RSVP status, and chatbot interactions.  
- City pages are generated dynamically from a list of routes, allowing new city pages to be added without modifying core routing logic.

### Database (SQLite)
- Guest RSVP data is stored in `wedding.db`.  
- The RSVP form validates input and updates the database in real time, allowing guests to confirm or change their attendance.  
- For advanced users, the database can be accessed directly using an SQLite browser to view or edit tables, though caution is advised to prevent unintentional changes.

### Chatbot
- A conversational chatbot lives in `weddingbot/` and handles guest inquiries interactively.  
- It recognizes the logged-in guest and addresses them by name, creating a personalized experience.  
- The chatbot answers questions about travel, registry, or the wedding schedule using a keyword-based system powered by `globals.py` and `main.py`.  
- Chat history is stored in the session, and its modular design allows future expansion without altering core app functionality.

### City Pages
- All travel and city information is under `templates/cities/` and styled consistently with `static/css/cities.css`.  
- Each city page features images, descriptions, and links to make it easy for guests to plan their visit.  
- New city pages can be added by copying an existing template, updating content and images, and adding the route to the city routes list in `app.py`.

### Static Assets
- All CSS, JavaScript, and images are served from the `static/` directory, keeping styling and interactivity consistent across the site.  
- JavaScript files handle countdown timers, chatbot interactivity, and other dynamic features, while CSS ensures themed and responsive layouts.

---

## 👰🤵 About

Developed by: Bill Klinkatsis
Purpose: To celebrate his and Marisa's wedding with a creative, interactive website for guests.
Company: ThrillBill International

"Made with love — and Flask."