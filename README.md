# Discovery Tracker

A web application for tracking and discovering music artists, their concert locations, dates, and more. Built with Go.

## Project Overview

Discovery Tracker is a full-stack web application developed in Go that fetches and displays information about music artists, including their concert locations, dates, and other details. The application uses the Groupie Tracker API to retrieve artist data and presents it in an intuitive user interface.

## Features

- **Artist Discovery**: Browse through a collection of artists with image thumbnails
- **Detailed Artist Pages**: View comprehensive information for each artist
- **Interactive Map**: View concert locations on an interactive Google Maps interface
- **Search Functionality**: Search for artists by name, creation date, first album, or location
- **Advanced Filtering**:
  - Filter by number of band members (1-8)
  - Filter by creation date range
  - Filter by first album date range
  - Filter by concert location

## Technologies Used

- **Backend**: Go (Golang)
- **Frontend**: HTML, CSS, JavaScript
- **Maps Integration**: Google Maps API
- **API Integration**: Groupie Tracker API
- **Concurrency**: Go routines and WaitGroups for parallel API requests

## Project Structure

```
├── api/
│   ├── fetchData.go    # API request handling
│   └── models.go       # Data models and structures
├── features/
│   ├── filterOption.go # Artist filtering functionality
│   ├── mapLocations.go # Google Maps integration
│   └── searchBar.go    # Search functionality
├── handlers/
│   ├── ArtistHandler.go # Handler for artist detail pages
│   ├── homeHandler.go   # Handler for home page
│   ├── parseTemplate.go # Template parsing utilities
│   └── serveFile.go     # Static file serving
├── static/
│   ├── css files        # Styling for the application
│   └── locationData.js  # Location data for filtering
├── templates/
│   ├── artist.html      # Artist detail page template
│   ├── home.html        # Home page template
│   └── notFoundPage.html # 404 page template
├── utils/
│   └── pageNotFound.go  # 404 handler
└── main.go              # Application entry point
```

## Key Learning Points

### 1. Go Web Development

- Implemented a complete web server using Go's standard library
- Used the `http` package to handle HTTP requests and routing
- Created a custom router using `HandleFunc` with HTTP method patterns
- Learned to serve static files and templates efficiently

### 2. Template Rendering

- Utilized Go's `html/template` package for rendering dynamic HTML
- Implemented proper error handling for template parsing and execution
- Passed structured data from Go to HTML templates

### 3. Concurrent Programming

- Leveraged Go's goroutines for parallel API requests
- Used `sync.WaitGroup` to coordinate concurrent operations
- Improved application performance by making API calls in parallel

### 4. API Integration

- Developed a reusable function for fetching API data
- Created structured models to represent API responses
- Handled JSON parsing and error management

### 5. Search and Filtering Implementation

- Built a comprehensive search function that works across multiple fields
- Implemented multi-criteria filtering with various data types
- Created user-friendly UI elements for search and filter operations

### 6. Frontend Integration

- Combined Go backend with HTML/CSS/JavaScript frontend
- Implemented responsive design for different device sizes
- Used JavaScript to enhance the user experience with dynamic elements

### 7. Maps Integration

- Integrated Google Maps API to display concert locations
- Implemented geocoding to convert location names to coordinates
- Created custom markers for artist performance venues

### 8. Error Handling

- Implemented proper error handling throughout the application
- Created custom error pages (404 Not Found)
- Added logging for debugging and monitoring

### 9. Code Organization

- Structured the project into logical packages (api, features, handlers, utils)
- Separated concerns between data models, business logic, and presentation
- Used Go's initialization function for setup operations

### 10. Responsive Design

- Implemented media queries for different screen sizes
- Created a mobile-friendly interface
- Optimized images and layout for various devices

---

This project provided invaluable experience in building a full-stack web application using Go, from handling API requests to creating an interactive user interface. The combination of Go's powerful concurrency features with frontend technologies resulted in a responsive and user-friendly application for music discovery.