# Portfolio — Cyberpunk Edition

A full-stack portfolio website with a neon cyberpunk frontend and PHP + MySQL backend. Features a complete admin panel for managing all site content.

## Tech Stack

- **Frontend**: Tailwind CSS v4 (CDN), custom cyberpunk CSS, JavaScript
- **Backend**: PHP 8, MySQL, PDO
- **Admin Panel**: Full CRUD, TinyMCE rich text editor, auth system
- **Design**: Neon cyan/pink cyberpunk theme, matrix rain, glitch text, scanlines

## Features

- Hero with matrix rain canvas + typing animation + glitch text
- Project showcase with alternating split layouts
- Skill bars with animated fill
- Experience timeline
- Testimonials with star ratings
- Blog with rich text content
- Contact form with validation
- Full admin panel with CRUD for all sections
- Responsive design

## Sections

| Section | Public | Admin |
|---------|--------|-------|
| Hero | ✅ Dynamic text | Settings |
| About | ✅ Bio + image | Settings |
| Skills | ✅ Category bars | CRUD |
| Projects | ✅ Cards + detail | CRUD |
| Services | ✅ Icon cards | CRUD |
| Experience | ✅ Timeline | CRUD |
| Testimonials | ✅ Quote cards | CRUD |
| Blog | ✅ Post list + detail | CRUD |
| Contact | ✅ Form | Inbox view |

## Installation

### 1. Setup Database
- Open phpMyAdmin (`http://localhost/phpmyadmin`)
- Import `database.sql` — creates `portfolio_db` with all tables and default data

### 2. Configure
- Edit `config/database.php` if your MySQL credentials differ from default (`root` / empty password)
- Edit `config/app.php` to set `SITE_URL` if needed

### 3. Deploy
- Copy the entire project folder to `C:\xampp\htdocs\portfolio`
- Start Apache + MySQL in XAMPP
- Visit `http://localhost/portfolio`

### 4. Admin Login
- URL: `http://localhost/portfolio/admin`
- Email: `admin@portfolio.com`
- Password: `Admin@123`

## Default Settings

Default setting keys stored in `site_settings` table:

| Key | Purpose |
|-----|---------|
| `site_title` | Brand name in header/footer |
| `site_subtitle` | Tagline under brand |
| `hero_title` | Main heading text |
| `hero_subtitle` | Text below heading |
| `hero_btn_text` | CTA button label |
| `hero_btn_link` | CTA button target |
| `about_title` | About section heading |
| `about_content` | About biography text |
| `about_image` | About section image URL |
| `footer_text` | Copyright line |
| `contact_email` | Contact form recipient |
| `github_url` | GitHub profile link |
| `linkedin_url` | LinkedIn profile link |
| `twitter_url` | Twitter profile link |
| `dribbble_url` | Dribbble profile link |
| `behance_url` | Behance profile link |
| `codepen_url` | CodePen profile link |

## File Structure

```
├── admin/              # Admin panel
│   ├── blog/           # Blog post CRUD
│   ├── dashboard.php   # Admin dashboard
│   ├── experience/     # Experience CRUD
│   ├── index.php       # Login page
│   ├── messages/       # Message inbox
│   ├── projects/       # Project CRUD
│   ├── services/       # Service CRUD
│   ├── settings/       # Site settings
│   ├── skills/         # Skill CRUD
│   └── testimonials/   # Testimonial CRUD
├── assets/
│   ├── css/style.css   # Cyberpunk theme styles
│   ├── js/main.js      # Frontend animations
│   └── uploads/        # Uploaded images
├── config/
│   ├── app.php         # Site constants
│   └── database.php    # DB connection
├── includes/
│   ├── admin_footer.php
│   ├── admin_header.php
│   ├── auth.php        # Auth helpers
│   ├── crud_helper.php # CRUD helpers
│   ├── footer.php      # Public footer
│   ├── functions.php   # DB query functions
│   └── header.php      # Public header
├── about.php
├── blog.php
├── blog-detail.php
├── contact.php
├── database.sql        # Schema + defaults
├── index.php           # Homepage
├── project-detail.php
├── projects.php
├── services.php
├── setup.php           # One-time setup
└── .htaccess           # URL rules
```

## Design Notes

- **Colors**: `#0a0a0f` (bg), `#00f0ff` (cyan accent), `#ff0080` (pink accent)
- **Fonts**: Space Grotesk (body), JetBrains Mono (code/UI)
- **Effects**: CSS scanlines, grid background, neon glow, glitch animation
- **No build step** — Tailwind v4 served via CDN, works directly in XAMPP

## Notes

- `setup.php` can be deleted after first run
- Admin panel uses the original glassmorphism theme (not cyberpunk)
- Images are stored in `assets/uploads/` when uploaded via admin
