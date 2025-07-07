# 🌤️ Weather Magic - Laravel React Weather Dashboard

A modern, full-stack weather dashboard application built with Laravel 12 backend and React 18 frontend. Features real-time weather data, AI-powered weather summaries, and secure authentication.

## 🚀 Features

- **🌐 Real-time Weather Data** - Get current weather for any city worldwide
- **🤖 AI Weather Summaries** - Intelligent weather insights powered by local LLM
- **🔐 Secure Authentication** - Laravel Sanctum-based login/register system
- **🎨 Modern UI/UX** - Beautiful, responsive design with weather-themed backgrounds
- **⚡ Fast Performance** - Built with Vite for lightning-fast development
- **📱 Mobile Responsive** - Works perfectly on all devices

## 🚀 Project Structure

- `backend/` — Laravel 12+ API backend
- `frontend/` — React 18+ frontend (Vite + TypeScript)

## Getting Started

### Backend (Laravel)

1. Install dependencies:
   ```bash
   cd backend
   composer install
   ```
2. Copy `.env.example` to `.env` and set your environment variables:
   ```bash
   cp .env.example .env
   ```
3. Generate application key:
   ```bash
   php artisan key:generate
   ```
4. Run migrations:
   ```bash
   php artisan migrate
   ```
5. Start the server:
   ```bash
   php artisan serve
   ```

#### Common Laravel Artisan Commands

- `php artisan serve` — Start the local development server
- `php artisan migrate` — Run database migrations
- `php artisan migrate:rollback` — Rollback the last database migration
- `php artisan db:seed` — Seed the database with test data
- `php artisan make:model ModelName` — Create a new Eloquent model
- `php artisan make:controller ControllerName` — Create a new controller
- `php artisan make:migration create_table_name` — Create a new migration file
- `php artisan make:seeder SeederName` — Create a new seeder
- `php artisan route:list` — List all registered routes
- `php artisan cache:clear` — Clear the application cache
- `php artisan config:cache` — Cache the configuration files
- `php artisan queue:work` — Process the next job on the queue
- `php artisan storage:link` — Create a symbolic link from public/storage to storage/app/public
- `php artisan tinker` — Interact with your application via the command line

### Frontend (React)

1. Install dependencies:
   ```bash
   cd frontend
   npm install
   # or
   yarn install
   ```
2. Start the development server:
   ```bash
   npm run dev
   # or
   yarn dev
   ```

## Usage
- The backend API will be available at `http://localhost:8000` by default.
- The frontend will be available at `http://localhost:3000` by default.

## Notes
- **Never commit your `.env` files or any secrets to version control.**
- For production, make sure to set up proper environment variables and secure your keys.

## License
MIT

## Local LLM (AI Model) Setup

This project uses a local Large Language Model (LLM) for AI weather summaries.

### Requirements
- [Ollama](https://ollama.com/) (or similar local LLM runner)
- Download the model you want to use (e.g., `tinyllama`, `mistral`)

### How to Run Locally

1. **Install Ollama**  
   Follow instructions at [https://ollama.com/download](https://ollama.com/download)

2. **Pull the model**  
   ```bash
   ollama pull tinyllama
   # or
   ollama pull mistral
   ```

3. **Start the Ollama server**  
   ```bash
   ollama serve
   ```

4. **Configure your `.env`**  
   ```
   OPENAI_BASE=http://localhost:11434/v1
   OPENAI_MODEL=tinyllama
   ```

5. **Restart your Laravel backend**  
   The backend will now use your local LLM for AI summaries.

### Changing the Model

- To use a different model, update `OPENAI_MODEL` in your `.env` and pull the model with Ollama.
