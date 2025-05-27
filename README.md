# Flask Auth0 App

**Name:** Satyam Panseriya

**Student ID :** 041128392  
**Email :** pans0012@algonquinlive.com  
**Video Link :** https://youtu.be/6t3Dp5O9oZ0

This is a simple Flask web application that integrates Auth0 for secure login, logout, and route protection. It demonstrates user authentication using OAuth2 and displays user profile information after login.

---

## Features

-  OAuth2 authentication with Auth0
-  Protected routes using session-based access
-  User profile display (name, picture, email)
-  Logout support with session cleanup
-  Environment-based configuration using `.env`

---

##  Prerequisites

Before you begin, make sure you have the following:

- ✅ Python 3.7 or later
- ✅ A free [Auth0](https://auth0.com/) account
- ✅ A terminal and basic understanding of Python

---

## Installation

1. **Clone the repository**

   ```bash
   git clone https://github.com/yourusername/flask-auth0-login-app.git
   cd flask-auth0-login-app
   
Create a virtual environment (recommended)

   ```bash

    python -m venv venv
    source venv/bin/activate     # macOS/Linux
    venv\Scripts\activate        # Windows
   ```


Install dependencies

```bash
pip install -r requirements.txt
```


 Auth0 Setup

1. Go to your Auth0 Dashboard.

2. Create a new Regular Web Application.

3. In the application Settings, set the following:

Allowed Callback URLs:

```bash
http://localhost:3000/callback
```

Allowed Logout URLs:

```bash
http://localhost:3000
```

Allowed Web Origins:

```bash
http://localhost:3000
```

Copy the following values for later use:

✅ Client ID

✅ Client Secret

✅ Domain (e.g., your-tenant-name.auth0.com)

## Environment Configuration

Create a `.env` file in the root directory of your project and add the following variables:

```env
AUTH0_CLIENT_ID=<Your Auth0 Client ID>
AUTH0_CLIENT_SECRET=<Your Auth0 Client Secret>
AUTH0_DOMAIN=<Your Auth0 Domain>
APP_SECRET_KEY=<Your Generated Secret Key>
```

### Generate a secure secret key:
```bash
openssl rand -hex 32
```

Copy the result and paste it into your .env file as the value for APP_SECRET_KEY.


 Running the App
To start the application, run:

```bash
python3 server.py
```
Then visit http://localhost:3000 in your browser.


