# Shelfio - Book Management Application

A modern book management application built with React, TypeScript, and Vite. Track your reading progress, manage collections, and organize your personal library.

## Features

- 📚 **Library Management**: Add, view, and manage your book collection
- 📖 **Reading Progress**: Track pages read and reading status
- ⭐ **Reviews & Ratings**: Rate and review your books
- 📁 **Collections**: Organize books into custom collections
- 🔍 **Search & Filter**: Find books by title, author, category, or status
- 📊 **Statistics**: View your reading statistics and progress

## Prerequisites

- Node.js (v18 or higher)
- npm (comes with Node.js)
- A backend API server running (see and check Backend URL configuration below)

## Installation

1. **Clone the repository**
   ```bash
   git clone <YOUR_GIT_URL>
   ```

2. **Navigate to the project directory**
   ```bash
   cd shelfoo
   ```

3. **Install dependencies**
   ```bash
   npm i
   ```

4. **Create environment file**
   ```bash
   # Create a .env file in the root directory
   touch .env
   ```

5. **Configure environment variables**
   
   Open the `.env` file and add your backend API URL:
   ```env
   VITE_API_BASE_URL=http://localhost:3000
   ```
   
   Replace `http://localhost:3000` with your actual backend API URL.

6. **Start the development server**
   ```bash
   npm run dev
   ```

7. **Open your browser**
   
   The application will be available at `http://localhost:5173` (or the port shown in your terminal)

## Environment Variables

Create a `.env` file in the root directory with the following variable:

```env
VITE_API_BASE_URL=your_backend_api_url_here
```

**Example:**
```env
VITE_API_BASE_URL=http://localhost:3000
```

Or for production:
```env
VITE_API_BASE_URL=https://api.yourdomain.com
```

> **Note**: If `VITE_API_BASE_URL` is not set, the app will use relative URLs (assuming the API is on the same domain).

## Available Scripts

- `npm run dev` - Start the development server
- `npm run build` - Build the application for production
- `npm run preview` - Preview the production build locally
- `npm run lint` - Run ESLint to check code quality

## Project Structure

```
shelfoo/
├── src/
│   ├── components/     # Reusable UI components
│   ├── pages/          # Page components
│   ├── hooks/          # Custom React hooks
│   ├── lib/            # Utility functions and helpers
│   ├── types/          # TypeScript type definitions
│   └── assets/         # Static assets
├── public/             # Public static files
├── .env               # Environment variables (create this file)
└── package.json       # Project dependencies
```

## Technologies Used

- **React 18** - UI library
- **TypeScript** - Type safety
- **Vite** - Build tool and dev server
- **Tailwind CSS** - Styling
- **shadcn/ui** - UI component library
- **React Router** - Routing
- **Lucide React** - Icons

## API Endpoints

The application expects the following API endpoints:

- `GET /api/books` - Get all books
- `GET /api/books/latest` - Get latest book
- `GET /api/books/recent` - Get recent books
- `GET /api/books/count` - Get total book count
- `POST /api/books` - Create a new book
- `PUT /api/books/{id}/pages-read` - Update pages read
- `PUT /api/books/{id}/status` - Update book status
- `POST /api/books/{id}/review` - Add/update review
- `DELETE /api/books/{id}` - Delete a book
- `GET /api/collections` - Get all collections
- `POST /api/collections` - Create a collection
- `DELETE /api/collections/{id}` - Delete a collection
- `POST /api/collections/{id}/books/{bookId}` - Add book to collection
- `DELETE /api/collections/{id}/books/{bookId}` - Remove book from collection
- `GET /api/stats/pages-read` - Get pages read statistics

## Development

1. Make sure your backend API is running
2. Update the `.env` file with the correct backend URL
3. Run `npm run dev` to start the development server
4. Make changes and see them hot-reload in the browser

## Building for Production

```bash
npm run build
```

The production build will be in the `dist/` directory.

## License

This project is private and proprietary.

## Support

For issues or questions, please contact the development team.
