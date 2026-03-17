# Fields M.D. - Easy Access to Children's Health Records

Fields M.D. is a secure, community-driven health portal that gives parents real-time access to their children’s medical records. Integrated with the Barangay Health Information System, it tracks key growth metrics like height, weight, and blood type via mobile or local kiosks. By simplifying health tracking, Fields M.D. enable parents to make informed decisions and stay engaged in their child’s care.


## Visual Preview
*(Add a GIF or screenshot of the UI here to show it actually works)*

## Key Features
- **Real-time Health Updates**: View key health indicators like height, weight, and blood type.
- **Seamless Integration**: Connects with the Barangay Health Information System.
- **Accessibility**: Designed for remote access on mobile devices or via self-service kiosks in local health centers.
- **Privacy & Security**: Ensures sensitive health information is accessible only to authorized users.

## 💻 Tech Stack

### Frontend
![Tailwind CSS](https://img.shields.io/badge/tailwindcss-%2338B2AC.svg?style=for-the-badge&logo=tailwind-css&logoColor=white)
![Vite](https://img.shields.io/badge/vite-%23646CFF.svg?style=for-the-badge&logo=vite&logoColor=white)
![Livewire](https://img.shields.io/badge/livewire-%234e56a6.svg?style=for-the-badge&logo=livewire&logoColor=white)

### Backend
![Laravel](https://img.shields.io/badge/laravel-%23FF2D20.svg?style=for-the-badge&logo=laravel&logoColor=white)
![PHP](https://img.shields.io/badge/php-%23777BB4.svg?style=for-the-badge&logo=php&logoColor=white)

### Database
![MySQL](https://img.shields.io/badge/mysql-%2300f.svg?style=for-the-badge&logo=mysql&logoColor=white)

### Local Server
![XAMPP](https://img.shields.io/badge/xampp-%23fb7a24.svg?style=for-the-badge&logo=xampp&logoColor=white)

## Getting Started

### Prerequisites
- PHP >= 8.1
- Composer
- Node.js & NPM
- Database (MySQL/PostgreSQL)

### Setting up Local Environment (XAMPP)
If you are using XAMPP for local testing, follow these specific steps:

1. **Install and Run XAMPP:** Open the XAMPP Control Panel and start the **Apache** and **MySQL** modules.
2. **Create Database:** Open your browser and navigate to `http://localhost/phpmyadmin`. Click on **Databases**, create a new database named `fields_md`, and click **Create**.
3. **Project Location:** Open your terminal. You can clone the project directly into your XAMPP htdocs directory:
   ```bash
   cd C:\xampp\htdocs
   git clone <repository-url> HCI-Fields-MD
   cd HCI-Fields-MD
   ```

### Installation & Configuration
1. **Install PHP and Node dependencies:**
   Make sure Composer and Node.js are installed on your system. Run these commands inside the `HCI-Fields-MD` project folder:
   ```bash
   composer install
   npm install
   ```

2. **Environment Setup:**
   Copy the example environment file and rename it to `.env`:
   ```bash
   cp .env.example .env
   ```
   Open the `.env` file and configure your database settings to match the one you created in phpMyAdmin:
   ```env
   DB_CONNECTION=mysql
   DB_HOST=127.0.0.1
   DB_PORT=3306
   DB_DATABASE=fields_md
   DB_USERNAME=root
   DB_PASSWORD=
   ```

3. **Generate Application Key:**
   ```bash
   php artisan key:generate
   ```

4. **Run Migrations and Seeders:**
   This will set up your database tables and populate them with initial data.
   ```bash
   php artisan migrate --seed
   ```

5. **Compile Frontend Assets:**
   ```bash
   npm run build
   ```

### Running the Application
Since you are using XAMPP, you have two options to view your project:

**Option 1: Using Apache (Directly via XAMPP)**
Open your browser and navigate to:
```text
http://localhost/HCI-Fields-MD/public
```

**Option 2: Using Artisan Serve (Recommended for Development)**
Run the local development server from your terminal:
```bash
php artisan serve
```
Then, open your browser and go to `http://localhost:8000`.

## Project Structure
A brief overview of the project structure:
- `app/` - Core logic, Models, and Controllers
- `routes/` - Web and API routing
- `resources/` - Views, CSS, and JS assets
- `public/` - Publicly accessible files (e.g., index.php, images)
- `database/` - Migrations and Seeders
