# Mealmate - Online Food Ordering System

Mealmate is a Django-based web application that enables users to register as either **restaurant owners** or **customers**. Restaurant owners can manage their restaurants, while customers can browse menus, place orders, and make secure payments using **Razorpay**.

## Features

### 🔐 Authentication
- User registration and login for both restaurant owners and customers
- Secure authentication using Django's built-in authentication system

### 🍽️ Restaurant Management
- Add new restaurants
- Edit and update restaurant details
- Delete restaurants

### 📋 Menu & Orders
- Customers can browse restaurant menus
- Add items to the cart
- Place orders

### 💳 Payment Integration
- Integrated **Razorpay** for secure online payments

---

## 🛠 Installation & Setup

### 1️⃣ Clone the Repository
```sh
git clone https://github.com/your-username/mealmate.git
cd mealmate
```

### 2️⃣ Set Up a Virtual Environment
```sh
python3 -m venv venv
source venv/bin/activate  # For Mac/Linux
venv\Scripts\activate    # For Windows
```

### 3️⃣ Install Dependencies
```sh
pip install -r requirements.txt
```

### 4️⃣ Apply Migrations
```sh
python manage.py migrate
```

### 5️⃣ Create a Superuser
```sh
python manage.py createsuperuser
```

### 6️⃣ Run the Development Server
```sh
python manage.py runserver
```
Now, open your browser and go to **http://127.0.0.1:8000/**

---

## 📂 Directory Structure
```
mealmate/
│── delivery/
│   │── migrations/
│   │── static/
│   │── templates/delivery/
│   │   ├── add_res.html
│   │   ├── base.html
│   │   ├── checkout.html
│   │   ├── cusmenu.html
│   │   ├── customer_home.html
│   │   ├── display_res.html
│   │   ├── failed.html
│   │   ├── index.html
│   │   ├── menu.html
│   │   ├── orders.html
│   │   ├── show_cart.html
│   │   ├── sign_in.html
│   │   ├── sign_up.html
│   │   ├── success.html
│   │   ├── userdata.html
│   │── __init__.py
│   │── admin.py
│   │── apps.py
│   │── forms.py
│   │── models.py
│   │── tests.py
│   │── views.py
│── manage.py
│── requirements.txt
```

---

## 📡 API Endpoints (If Using Django REST Framework)

| Method | Endpoint | Description |
|--------|----------|-------------|
| GET    | `/restaurants/` | List all restaurants |
| POST   | `/restaurants/add/` | Add a new restaurant |
| PUT    | `/restaurants/update/<id>/` | Update restaurant details |
| DELETE | `/restaurants/delete/<id>/` | Delete a restaurant |
| GET    | `/menu/` | Get menu items |
| POST   | `/order/` | Place an order |

---

## 💰 Razorpay Payment Integration

1. Sign up at [Razorpay](https://razorpay.com/)
2. Get API keys from Razorpay Dashboard
3. Add API keys to Django settings:

```python
RAZORPAY_KEY_ID = "your_key_id"
RAZORPAY_KEY_SECRET = "your_key_secret"
```

---

## 🚀 Contributing
Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

---

## 📜 License
This project is licensed under the [MIT License](LICENSE).

---

## ✨ Acknowledgments
Special thanks to all contributors and open-source resources that helped build this project.
