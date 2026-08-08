# Social Media Platform

A full-stack **Django social media web application** inspired by platforms like Twitter and Instagram. Users can create accounts, follow other users, share image posts, like posts, discover new users and content, and customize their profiles.

The project uses **Django** for the backend and **HTML, CSS, JavaScript, and Bootstrap** for the frontend.

---

## 🚀 Features

### 👤 User Authentication

* User registration and account creation
* User login and logout
* Secure authentication using Django's authentication system
* User profile creation

### 👥 Follow System

* Follow other users
* Unfollow users
* View users you follow
* Build your own social network
* Similar following experience to Twitter and Instagram

### 🖼️ Posts

* Create posts with images
* Upload images from your device
* View posts from other users
* Display posts in the user's feed
* Explore posts from other users

### ❤️ Like System

* Like posts
* Unlike posts
* Display the number of likes on posts
* Users can interact with posts from other users

### 👨‍💻 User Profiles

Users can customize their profile with:

* Profile photo
* Bio
* Location
* Username
* Followers
* Following
* User posts

### 🔎 User Search

* Search for other users using a search box
* Search by username
* Open another user's profile
* Follow or unfollow users directly from their profile

### 🌎 Explore

The application includes an **Explore** section where users can discover:

* Posts from other users
* New users
* Images shared by the community
* Content outside their own following list

### 📱 Responsive Design

The frontend is built using:

* HTML5
* CSS3
* JavaScript
* Bootstrap

The application is designed to work across desktop, tablet, and mobile screen sizes.

---

## 🛠️ Technologies Used

### Backend

* Python
* Django
* Django ORM
* SQLite / PostgreSQL

### Frontend

* HTML5
* CSS3
* JavaScript
* Bootstrap

### Other

* Django Templates
* Django Authentication
* Django Media Files
* Image Uploads

---


## ⚙️ Installation

Follow these steps to run the project locally.

### 1. Clone the Repository

```bash
git clone https://github.com/your-username/social-media-project.git
```

Move into the project directory:

```bash
cd social-media-project
```

---

### 2. Create a Virtual Environment

Create a Python virtual environment:

```bash
python -m venv venv
```

Activate it.

#### Windows

```bash
venv\Scripts\activate
```

#### macOS / Linux

```bash
source venv/bin/activate
```

---

### 3. Install Dependencies

Install the required Python packages:

```bash
pip install -r requirements.txt
```

If you don't have a `requirements.txt` file yet, you can install Django with:

```bash
pip install django
```

---

### 4. Configure the Database

Run Django migrations:

```bash
python manage.py makemigrations
python manage.py migrate
```

---

### 5. Create a Superuser

Create an admin account:

```bash
python manage.py createsuperuser
```

Follow the instructions in the terminal.

---

### 6. Run the Development Server

Start the Django development server:

```bash
python manage.py runserver
```

Open your browser and visit:

```text
http://127.0.0.1:8000/
```

The Django admin panel can be accessed at:

```text
http://127.0.0.1:8000/admin/
```

---

## 🔐 Authentication

The project uses Django's built-in authentication functionality.

Users can:

1. Create an account
2. Log in
3. Log out
4. Access their profile
5. Follow other users
6. Create posts
7. Like posts
8. Search for users

---

## 📸 Creating a Post

A logged-in user can create a post by uploading an image.

A typical post contains:

```text
User
Image
Created Date
Likes
```

Example:

```text
┌──────────────────────────────┐
│  👤 username                 │
│                              │
│       [ Post Image ]         │
│                              │
│  ❤️ 25 Likes                 │
│                              │
│  Posted 2 hours ago          │
└──────────────────────────────┘
```

---

## 👥 Following Users

Users can search for another username and visit their profile.

From the profile page, they can:

```text
Follow
```

or

```text
Unfollow
```

The profile can display:

```text
Posts     Followers     Following
```

---

## 🔎 Search

The search functionality allows users to find other accounts by username.

Example:

```text
Search: john
```

Possible results:

```text
John
john_doe
john123
john_smith
```

Users can select a result to view the user's profile.

---

## 🌎 Explore Page

The Explore page allows users to discover content from across the platform.

Unlike the main feed, which can focus on users they follow, the Explore page can show posts from the wider community.

Example:

```text
                 Explore

 ┌──────────┐ ┌──────────┐ ┌──────────┐
 │  Image   │ │  Image   │ │  Image   │
 │          │ │          │ │          │
 │ ❤️ 120   │ │ ❤️ 80    │ │ ❤️ 45    │
 └──────────┘ └──────────┘ └──────────┘
```

---

## 👤 Profile Customization

Users can edit their profile information.

They can update:

* Profile picture
* Bio
* Location

Example:

```text
┌─────────────────────────────────┐
│          Profile Photo           │
│                                 │
│          @username              │
│                                 │
│  📍 Mumbai, India               │
│                                 │
│  "Photography & travel 📷"      │
│                                 │
│  Posts  24   Followers  150     │
│          Following  80          │
└─────────────────────────────────┘
```

---

## 🗃️ Media Files

User-uploaded files are stored using Django's media-file configuration.

Typical media directories:

```text
media/
├── profile_images/
└── post_images/
```

Make sure your Django settings contain the appropriate `MEDIA_URL` and `MEDIA_ROOT` configuration.

For development, configure your project URLs to serve media files when `DEBUG=True`.

---

## 🧩 Main Models

A typical implementation can contain models such as:

### User / Profile

Stores additional information about the user.

```text
Profile
├── user
├── profile_image
├── bio
└── location
```

### Post

Stores posts created by users.

```text
Post
├── user
├── image
└── created_at
```

### Follow

Stores relationships between users.

```text
Follow
├── follower
└── following
```

### Like

Stores likes on posts.

```text
Like
├── user
├── post
└── created_at
```

The exact models and fields may differ depending on the implementation.

---

## 🎨 Frontend

The frontend is developed using:

### HTML

Used to create the structure of pages and components.

### CSS

Used for custom styling and visual design.

### JavaScript

Used for client-side interactions and dynamic behavior.

### Bootstrap

Used for:

* Responsive layouts
* Navigation bars
* Buttons
* Cards
* Forms
* Modals
* Grid layouts
* Mobile responsiveness

---

## 🔑 Important Django Concepts Used

This project demonstrates several important Django concepts:

* Django Models
* Django Views
* Django Templates
* Django Forms
* URL Routing
* Authentication
* Django ORM
* Model Relationships
* File/Image Uploads
* Static Files
* Media Files
* Template Inheritance
* CSRF Protection
* Admin Panel

---

## 🔄 Application Flow

```text
                    ┌──────────────┐
                    │    User      │
                    └──────┬───────┘
                           │
              ┌────────────┴────────────┐
              │                         │
         Create Account              Login
              │                         │
              └────────────┬────────────┘
                           │
                      Home / Feed
                           │
          ┌────────────────┼────────────────┐
          │                │                │
       Create Post      Search           Explore
          │                │                │
          │                │          Discover Posts
          │                │
          │           Find User
          │                │
          │             Follow
          │
       Upload Image
          │
        Like Post
          │
       View Profile
          │
   Edit Photo / Bio / Location
```


